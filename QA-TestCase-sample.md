<h3>Test Case: End-to-End Payment to Philippines via PhilGov Service</h3>
Test Case ID: PAY-PHIL-TP-TC001

Objective: Verify the end-to-end payment flow to the Philippines using PhilGov Service works as expected, ensuring correct status updates to "Fully Paid."
<hr>

<strong>Test Steps</strong>

Preconditions:
<ul>
<li>User has a valid PhilGov account.</li>
<li>Test environment is set up with API endpoints for PhilGov Service.</li>
<li>Test data includes valid payment details (e.g., reference ID, amount).</li>
</ul>

<table>
<tr><td>Step No.</td><td>Action	Expected</td><td>Result</td></tr>
<tr><td>1</td><td>Log in to the system as a user.</td><td>User is successfully logged in and redirected to the dashboard.</td></tr>
<tr><td>2</td><td>Navigate to the payment page and select "Philippines" as the destination country.</td><td>The option to pay via PhilGov Service is visible in the payment methods list.</td></tr>
<tr><td>3</td><td>Select "PhilGov Service" and proceed to the payment details page.</td><td>Payment details form appears with fields for Reference ID, Amount, and Purpose of Payment.</td></tr>
<tr><td>4</td><td>Enter valid payment details (e.g., REF12345, PHP 10000, "Government Fees").</td><td>Form is validated, and the "Proceed to Payment" button is enabled.</td></tr>
<tr><td>5</td><td>Click "Proceed to Payment" and authenticate using the OTP sent by PhilGov Service.</td><td>OTP is verified, and user is redirected back to the application with a status of "Pending Confirmation."</td></tr>
<tr><td>6</td><td>Simulate API callback from PhilGov Service with the status of Confirmed.</td><td>Payment status in the system updates to "Confirmed."</td></tr>
<tr><td>7</td><td>Verify the system changes the payment status to "Fully Paid" and generates a receipt.</td><td>Payment status changes to "Fully Paid," and receipt is available for download.</td></tr>
<tr><td>8</td><td>Download and verify the receipt for accuracy (e.g., payment amount, reference ID, date).</td><td>	Receipt details match the transaction, and the file is downloaded successfully.</td></tr>
</table>

<strong>Test Data</strong>
<table><tr><td>Field</td><td>Value</td></tr>
<tr><td>Destination</td><td>Philippines</td></tr>
<tr><td>Payment Method</td><td>PhilGov Service</td></tr>
<tr><td>Reference ID</td><td>REF12345</td></tr>
<tr><td>Amount</td><td>PHP 10,000</td></tr>
<tr><td>Purpose	Government</td><td>Fees</td></tr>
</table>

Expected Outputs
UI Output : Payment status transactions: "Pending Confirmation" -> "Confirmed" -> "Fully Paid". Receipt is generated with correct details.

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
