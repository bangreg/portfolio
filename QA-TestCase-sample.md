<h3>Test Case: End-to-End Payment to Philippines via PhilGov Service</h3>
Test Case ID: PAY-PHIL-TP-TC001

Objective: Verify the end-to-end payment flow to the Philippines using PhilGov Service works as expected, ensuring correct status updates to "Fully Paid."
<hr>
<h3Test Steps></h3>
Preconditions:
<ul>
<li>User has a valid PhilGov account.</li>
<li>Test environment is set up with API endpoints for PhilGov Service.</li>
<li>Test data includes valid payment details (e.g., reference ID, amount).</li>
</ul>

<table>
<tr><td>Step No.</td><td>Action	Expected</td><td>Result</td></tr>
1	Log in to the system as a user.	User is successfully logged in and redirected to the dashboard.
2	Navigate to the payment page and select "Philippines" as the destination country.	The option to pay via PhilGov Service is visible in the payment methods list.
3	Select "PhilGov Service" and proceed to the payment details page.	Payment details form appears with fields for Reference ID, Amount, and Purpose of Payment.
4	Enter valid payment details (e.g., REF12345, PHP 10000, "Government Fees").	Form is validated, and the "Proceed to Payment" button is enabled.
5	Click "Proceed to Payment" and authenticate using the OTP sent by PhilGov Service.	OTP is verified, and user is redirected back to the application with a status of "Pending Confirmation."
6	Simulate API callback from PhilGov Service with the status of Confirmed.	Payment status in the system updates to "Confirmed."
7	Verify the system changes the payment status to "Fully Paid" and generates a receipt.	Payment status changes to "Fully Paid," and receipt is available for download.
8	Download and verify the receipt for accuracy (e.g., payment amount, reference ID, date).	Receipt details match the transaction, and the file is downloaded successfully.
</table>
Test Data
Field	Value
Destination	Philippines
Payment Method	PhilGov Service
Reference ID	REF12345
Amount	PHP 10,000
Purpose	Government Fees
Expected Outputs

    UI Output:
        Payment status transitions: "Pending Confirmation" → "Confirmed" → "Fully Paid".
        Receipt is generated with correct details.

    API Callback Output:

    {
        "payment_id": "5678",
        "status": "Confirmed",
        "transaction_reference": "PHGOV-12345",
        "timestamp": "2024-12-20T10:00:00Z"
    }

    Database Entry:
        Payment status in payments table updates to Fully Paid.

    Email Notification:
        Subject: "Payment Confirmation - Fully Paid."
        Body: "Your payment to the Philippines using PhilGov Service has been successfully processed."

Pass/Fail Criteria:

    Pass: All steps execute successfully with outputs matching expected results.
    Fail: Any deviation in status updates, API responses, receipt details, or user notifications.

Postconditions:

    Payment is marked as completed in the database.
    Receipt is downloadable and stored in the system.
