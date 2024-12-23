Here's an example of a Selenium testing script in Java for the website https://the-internet.herokuapp.com/. The test performs the following steps:
<ul>
<li>Open the homepage of the site.</li>
<li>Verify the presence of the main title, "Welcome to the-internet."</li>
<li>Navigate to the "Form Authentication" page via the provided link.</li>
<li>Verify that the "Login Page" is displayed.</li>
</ul>
<hr>
Java Selenium Code Example

    import org.openqa.selenium.By;
    import org.openqa.selenium.WebDriver;
    import org.openqa.selenium.WebElement;
    import org.openqa.selenium.chrome.ChromeDriver;
    import org.openqa.selenium.chrome.ChromeOptions;
    import org.openqa.selenium.support.ui.WebDriverWait;
    import org.openqa.selenium.support.ui.ExpectedConditions;

    import java.time.Duration;

    public class HerokuAppTest {
        public static void main(String[] args) {
            // Set up the path to ChromeDriver
            System.setProperty("webdriver.chrome.driver", "path_to_chromedriver");
    
            // Initialize WebDriver
            ChromeOptions options = new ChromeOptions();
            options.addArguments("--start-maximized");
            WebDriver driver = new ChromeDriver(options);
    
            try {
                // 1. Open the main page
                driver.get("https://the-internet.herokuapp.com/");
                WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    
                // 2. Verify the page title
                WebElement titleElement = driver.findElement(By.tagName("h1"));
                String titleText = titleElement.getText();
                assert titleText.equals("Welcome to the-internet") : "Title mismatch: " + titleText;
                System.out.println("Title found: " + titleText);
    
                // 3. Click the "Form Authentication" link
                WebElement formAuthLink = driver.findElement(By.linkText("Form Authentication"));
                formAuthLink.click();
    
                // Wait for the "Login Page" to load
                wait.until(ExpectedConditions.presenceOfElementLocated(By.tagName("h2")));
    
                // 4. Verify the "Login Page" is displayed
                WebElement pageTitleElement = driver.findElement(By.tagName("h2"));
                String pageTitleText = pageTitleElement.getText();
                assert pageTitleText.equals("Login Page") : "Page mismatch: " + pageTitleText;
                System.out.println("Login Page opened: " + pageTitleText);
    
            } catch (Exception e) {
                e.printStackTrace();
            } finally {
                // 5. Close the browser
                driver.quit();
            }
        }
    }
<hr>    
Code Explanation
<ol>
    <li>Driver Setup:</li>
    <ul>
        <li>System.setProperty specifies the location of the ChromeDriver.</li>
        <li>ChromeOptions configures the browser to start maximized.</li>
    </ul>
    <li>Test Steps:</li>
    <ul>
        <li>Opens the main page of the-internet.herokuapp.com.</li>
        <li><Finds elements using locators like By.tagName and By.linkText.</li>
        <li>Navigates to the Form Authentication page and waits until it fully loads.</li>
    </ul>
    <li>Assertions:</li>
        <ul>
        <li>Uses assert to check if the retrieved text matches the expected values.</li>
        <li>If the assertion fails, the script will stop with an error.</li>
        </ul>
    <li>WebDriverWait:</li>
        <ul>
        <li>Ensures that elements are present before interacting with them, avoiding errors due to elements not being fully loaded.</li>
        </ul>
    <li>Finally Block:</li>
    <ul>
        <li>Guarantees the browser is closed after the test, even if an error occurs.</li>
    </ul>
</ol>
<hr>
How to Run the Script
<ol>
    <li>Requirements:</li>
    <ul>
        <li>Java installed on your system.</li>
        <li>ChromeDriver matching your Chrome browser version.</li>
        <li>Maven (optional, for dependency management).</li>
    </ul>
    <li>Using Maven:</li>
    Add Selenium dependencies to your pom.xml:
    </ul>

    <dependencies>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>4.14.0</version>
        </dependency>
    </dependencies>

<li>Running the Script:</li>
<ul>   
    <li>Save the file as HerokuAppTest.java.</li>
    <li>Compile and run:</li>
</ol>

    javac HerokuAppTest.java
    java HerokuAppTest
<hr>
Expected Output

If the script executes successfully, it will print:

    Title found: Welcome to the-internet
    Login Page opened: Login Page
