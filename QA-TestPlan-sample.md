<h3>Test Plan: Payment to Philippines via PhilGov Service</h3>
<ol><li>Test Plan ID</li>
PAY-PHIL-TP001<br><br>

<li>Objective</li>
To ensure the payment flow to the Philippines via the PhilGov service is functioning correctly, meeting all functional and non-functional requirements, from initiation to confirmation of a "Fully Paid" status.<br><br>

<li>Scope</li>
In-Scope:
Payment flow using the PhilGov service.
Functional testing (form submission, API callbacks, status updates).
User interface elements (buttons, form validation, receipt generation).
Integration testing with PhilGov API.
Cross-browser testing (e.g., Chrome, Safari, Edge).

Out-of-Scope:
Other payment gateways (e.g., PayPal, Stripe).
Non-Philippines payment destinations.
Load testing of PhilGov servers.

<li>Test Strategy</li>
Testing Levels:
Unit Testing for backend payment logic.
Integration Testing for API communication with PhilGov.
End-to-End (E2E) Testing for full user journey.

Testing Types:
Functional Testing (form validation, flow correctness).
API Testing (response codes, data validation).
Negative Testing (invalid inputs, failed authentication).
Regression Testing (ensuring no disruption in existing features).
Automation Approach:
Automate repetitive tasks like regression tests using Playwright.
Manual testing for scenarios involving UI elements or edge cases.

<li>Test Environment</li>
Devices: Laptop, mobile (Android, iOS).
Browsers: Chrome, Edge, Safari (latest versions).

Test Data:
Valid PhilGov account credentials.
Sample payment amounts (PHP 1,000, PHP 10,000).
Mock API responses for edge cases.

<li>Test Schedule</li>
<table>
<tr>
  <td>Phase</td>
  <td>Start Date</td>
  <td>End Date</td>
  <td>Responsible</td>
  
</tr>
<tr>
  <td>Test Case Preparation</td>
  <td>2024-12-20</td>
  <td>2024-12-22</td>
  <td>QA Engineer</td>
</tr>
<tr>
  <td>Functional Testing</td>
  <td>2024-12-23</td>
  <td>2024-12-25</td>
  <td>QA Engineer</td>
</tr>
<tr><td>Integration Testing</td><td>2024-12-26</td><td>2024-12-27</td><td>Dev + QA</td></tr>
<tr><td>Regression Testing</td><td>2024-12-28</td><td>2024-12-29</td><td>Automation</td></tr>
<tr><td>Final Validation (UAT)</td><td>2024-12-30</td><td>2024-12-30</td><td>QA + Users</td></tr>
</table>

<li>Test Deliverables</li>
Test Cases (functional, integration, regression).
Bug reports in JIRA.
Test Summary Report after execution.
Screenshots/logs of critical issues.<br><br>

<li>Risks and Mitigation</li>
Risk	Mitigation
PhilGov API downtime	Use mock API to simulate responses.
Delayed receipt generation	Test with smaller transaction amounts for faster validation.
Complex edge cases not accounted for	Conduct exploratory testing and add cases iteratively.<br><br>

<li>Entry and Exit Criteria</li>
Entry Criteria:
Payment feature development is complete.
PhilGov API is integrated and stable.

Exit Criteria:
100% of test cases executed with a 95% pass rate.
All critical and high-severity bugs are resolved.
UAT approval from stakeholders.

<li>Approvals</li>
Test Plan Prepared By: QA Engineer
Approved By: QA Lead, Project Manager
</ol>
