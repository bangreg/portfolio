<h3>Release Notes</h3>

Feature Name: Payment to Philippines via PhilGov Service
Release Version: 1.0.0
Release Date: 2024-12-22
<hr>
1. New Features
<ul>
    Philippines Payment Integration:
        <li>Users can now make payments to the Philippines using the PhilGov Service.</li>
        <li>Supports payments for government-related purposes such as taxes, fees, and permits.</li>
  <br>
  End-to-End Payment Status Tracking:
        <li>Payment statuses: Pending Confirmation, Confirmed, and Fully Paid.</li>
        <li>Real-time updates based on PhilGov API callbacks.</li>
  <br>
  Receipt Generation:
        <li>Automated receipt generation after payment completion.</li>
        <li>Receipts are downloadable via a secure link.</li>
  <br>
  OTP Verification:
        <li>Enhanced security with OTP authentication during the payment process.</li>
  </ul>
  <hr>
2. Enhancements
    UI/UX Improvements:
        <ul>
            <li>Streamlined payment form with user-friendly validation messages.</li>
            <li>Clear status indicators for each payment stage.</li>
        </ul>
    <br>
    API Performance Optimization:
        <ul>
            <li>Improved response times for PhilGov API requests.</li>
            <li>Enhanced error handling for edge cases (e.g., network timeouts).</li>
        </ul>
<hr>
3. Bug Fixes
<ul>
    <li>Fixed an issue where invalid reference IDs caused form freezing.</li>
    <li>Corrected currency symbol alignment on the payment page.</li>
    <li>Resolved API error mapping for unsupported government services.</li>
</ul>
<hr>
4. Known Issues
    Issue: 
        <ul><li>Receipt download may take longer on mobile devices using slower networks.</li>
        <li>Workaround: Users can retry download on a stable connection.</li></ul>
    Issue: <ul><li>Edge browser users may experience layout misalignment on the payment page.</li>
        <li>Workaround: Recommended browsers: Chrome, Safari.</li></ul>
<hr>
5. Technical Details
    API Endpoint for PhilGov Service:
        <ul><li>/api/v1/philgov/payments</li>
        <li>Supports both test and production environments.</li></ul>
    Logs and Monitoring:
        <ul>
        <li>All payment transactions are logged in the system for auditing purposes.</li>
        <li>Integrated monitoring with tools like Nagios for real-time performance tracking.</li></ul>
<hr>
6. Deployment Notes
<ul>
    <li></li>Database Update: New table philgov_transactions added to store payment data.li>
    <li>Downtime Impact: No expected downtime.</li> 
    <li>Rollout Plan: Gradual rollout over a 24-hour window to monitor live performance.</li>
</ul>
<hr>
7. Contact Information
For support or to report an issue:
    Email: support@example.com
    Phone: +1-800-123-4567
