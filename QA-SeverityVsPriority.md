<h3>Severity</h3>

Severity levels for various issues in an application from a QA perspective.<br>		
Severity levels depend on:		
1. Impact on end-users.		
2. Functions affected (core or auxiliary).		
3. Risk to the application or business.		
		
S1. Critical Severity<br>		
Definition:		
Issues with a severe impact, such as data loss or significant security breaches.		
Examples:		
1. Data leakage of sensitive user information.		
2. A complete breakdown of the core application for all users.	<br>	
Impact:		
1. Must be fixed immediately, outside regular maintenance schedules.		
2. Can lead to severe legal, financial, or operational consequences.		
		
			
S2. Major Severity<br>		
Definition:		
Critical issues that directly impact the core functionality of the application, leading to major disruptions or preventing users from completing essential tasks.		
Examples:		
1. System crashes when a user attempts to log in.		
2. Key features (e.g., payment processing or file uploads) are completely non-functional.<br>		
3. Security vulnerabilities (e.g., passwords displayed in plaintext).		
Impact:		
1. Prevents users from completing primary tasks.		
2. Can result in financial, reputational, or security risks.		
		
	
S3. Moderate Severity	<br>	
Definition:		
Issues that affect part of the application’s functionality or user experience but have workarounds available.		
Examples:		
1. A button is not functioning, but the same action can be performed elsewhere.		
2. Error messages are unclear or misleading (e.g., "Invalid request" without details).		
3. Slow application response for specific actions but no crashes.		<br>
Impact:		
1. Causes inconvenience to users.		
2. May affect certain tasks, but the application remains usable.		
		
		
		
S4. Low Severity	<br>	
Definition:		
Issues with minimal impact on application functionality that do not significantly affect the user experience.		
Examples:		
1. Typographical errors (e.g., "Welcom" instead of "Welcome").		
2. Slight misalignment of UI elements.		
3. Incorrect color or icon that doesn’t affect functionality.	<br>	
Impact:		
1. Does not disrupt the overall user experience.		
2. Has no effect on core application workflows.		


<h3>Priority</h3>
How to determine priority levels (Critical, High, Medium, Low) for a bug, based on Business urgency, Impact on users, Release deadlines, Availability of workaround		<br>			
1. Business Impact: Does this bug affect key metrics, such as revenue or customer satisfaction?			<br>
2. Number of Users Affected: Does it impact a majority of users or just a small group?			<br>
3. Release Deadlines: Does the bug block a new feature or need fixing before a critical deadline?		<br>	
4. Availability of Workaround: Can users continue with an alternative solution?			<br><br>
			
P1. Critical Priority				<br>		
Definition:			
The bug must be fixed immediately because it causes a major disruption in core functionality or poses a serious risk.		<br>	
Characteristics:			
1. Affects all users or a majority of users.			<br>
2. There is no workaround to continue the process.			<br>
3. Blocks release or production until resolved.		<br>	
Examples:			<br>
1. System crashes when logging in or during payment.		<br>	
2. Security vulnerability exposing customer data.		<br>	
3. A core feature (e.g., purchase or file upload) is non-functional.		<br>	
			
			
			
P2. High Priority				<br>	
Definition:			
The bug significantly impacts the application or user experience and must be fixed before a major release or update.			<br>
Characteristics:			
1. Impacts important functionality but doesn’t stop the entire operation.		<br>	
2. A workaround may exist but is not ideal.			<br>
Examples:			<br>
1. Submit button not working in a critical form.			<br>
2. Incorrect error messages on important actions.		<br>	
3. API delays causing slow application responses in key features.	<br>		
			
			
			
P3. Medium Priority				<br>	
Definition:			
The bug is not urgent but still needs to be fixed within a certain timeframe, usually in an upcoming release.		<br>	
Characteristics:			
1. Does not affect core functionality.			<br>
2. Impacts a small portion of users or non-critical areas.			<br>
3. Users can continue tasks with minor inconvenience.		<br>	
Examples:			<br>
1. UI design is inconsistent but doesn’t affect functionality.		<br>	
2. Error occurs in a rarely used report or feature.			<br>
3. Application is slow for secondary features.			<br>
			
			
			
P4. Low Priority				<br>	
Definition:			
The bug has minimal impact on user experience and is not urgent to fix.			<br>
Characteristics:			
1. Cosmetic or minor issues with no impact on functionality.	<br>		
2. Does not affect core processes or business flows.	<br>		
Examples:			<br>
1. Typo on a page rarely visited by users.	<br>		
2. Incorrect icon in a non-essential UI element.	<br>		
3. Mismatched colors or fonts not adhering to brand guidelines.	<br>		


