# PROJECT TITLE: Auzmor UI Automation Framework

## LINK: [[Auzmor Application](https://office-qa.auzmor.com/login)](https://office-qa.auzmor.com/login
)

### Credentials:
- Username: dohutoja.ohabufi@jollyfree.com
- Password: Password1@

## PROBLEM STATEMENT SCENARIO:

### Navigate to the Social Feed:
1. Open the application.
2. Locate and click on the "Feed" tab.

### Create a Poll:
3. Click on the "What’s on your mind" section to initiate a new post.
4. Add Post Content.
5. Look for the "Polls" Call-to-Action (CTA) and click on it.
6. Enter a relevant poll question.
7. Add at least two poll options.
8. Select a poll duration.
9. Click on the "Add a poll" button.

### Submit the Poll:
10. Click on the "Submit Post" button to publish the poll.

### Verify Poll Visibility:
11. Return to the Social Feed.
12. Check if the submitted poll is visible on the feed page.

### Additional Verifications:
13. Verify that the poll cannot be submitted without a valid question.
14. Verify that the poll cannot be submitted with insufficient options.
15. Check if the submitted poll is visible on the feed page.


## OVERVIEW:

This repository contains an automated testing framework designed for the Auzmor application. The framework aims to provide a scalable, maintainable, and platform-independent solution for testing the creation and submission of polls in the social feed.

## PREREQUISITES:

Before running the tests, ensure you have the following installed:

- Java Development Kit (JDK)
- Maven
- Selenium
- TestNG
- Chrome Browser

## REQUIREMENTS:

- Programming Language: Java
- Automation Tool: Selenium
- Browser Compatibility: Chrome
- Platform Independence: Windows, macOS, Linux
- Framework Structure: Page Object Model (POM), Singleton Pattern
- Test Execution: TestNG with parallel test support
- Configuration: Configurable parameters via properties file
- Logging: Include appropriate logging to capture events and errors

## To Start Execution:

### SETUP

1. Clone the repository: `git clone https://github.com/Poojitha1316/MiniProject.git`
2. Navigate to the project directory: `cd social-feed-automation`
3. Install dependencies: `mvn clean install`

## FRAMEWORK STRUCTURE:

The framework follows the Page Object Model (POM) design pattern and includes:

- **BaseTest Package:** BaseTest contains the BaseClass with common methods for navigating and interacting with the application.

- **PageObjects Package:** It contains all the page classes representing different pages of the Social Feed application.
  - **FeedPage:** Page class for interacting with the Social Feed.
  - **LoginPage:** Page class for logging into the Auzmor website.
  - **PollCreationPage:** Page class for creating and submitting polls.
  - **VerifySubmittedPollPage:** Page class for verifying the submitted poll.

- **Utilities Package:** Utility package for handling common functionalities.
  - **ReadPropertiesFile:** Reads configuration properties from the config.properties file.
  - **UtilityFile:** Handles screenshot functionalities.

- **TestCases:** Test class implementing scenarios for auzmor automation.
  - **FeedPostProcessTest** Test class for creating and verifying the polls.
  - **QuestionOptionsVerificationTest** Test class for verifying question and options with sufficient details.

- **pom.xml:** It contains configuration information related to the project's build process, dependencies, plugins, and other settings.

- **Screenshots:**
Captures the screenshots in case of failures.

## PROJECT INFORMATION:

- **Group ID:** Identifies the project's group.
- **Artifact ID:** Specifies the project's unique identifier.
- **Version:** Represents the version of the project.

## DEPENDENCIES:

- Selenium WebDriver (Latest Version): Selenium is a powerful tool for controlling web browsers through programs and performing browser automation.
- Log4j (Latest Version): Log4j is a logging library for Java.
- JUnit or TestNG (Latest Version): Testing frameworks for running tests.
- WebdriverManager (Latest Version): WebDriverManager is a library that helps automate the management of the binary drivers required by Selenium WebDriver.

## WORKING PROCESS:

### TEST CASE-1 (Navigate to Social Feed and Create Poll):

**BeforeMethod:** (performLoginAndNavigateToFeed):

 - Initializes the WebDriver and opens the browser.
 - Logs into the application using login credentials specified in the loginDetails method of the LoginPage.
 - Navigates to the Feed page using the feedDetails method of the FeedPage.

**Test Method:** (testFeedPostProcess):
 
 - Performs the actual test by creating a new poll using the PollCreation page.

**AfterMethod:** (verifySubmittedPoll):

 - Verifies the submitted poll result by calling the verifyResult method of the VerifySubmittedPoll page.

### TEST CASE-2 (Question Options Verification Test):

**BeforeMethod:** (loginAndNavigateToFeed):

 - Initializes the WebDriver and opens the browser.
 - Logs into the application using login credentials specified in the loginDetails method of the LoginPage.
 - Navigates to the Feed page using the feedDetails method of the FeedPage.

**Test Methods:**

 - testEmptyAndCharacterQuestions: Creates two instances of PollCreation to verify submissions with an empty question and a character in the question.
 - testInsufficientOptions: Creates an instance of PollCreation to verify submission with insufficient options.

**AfterMethod:** (captureScreenshotOnFailure):

 - Captures a screenshot using the takingScreenshot method from the Utility class in case of test failure.

### General Notes:

- Both test cases share a common setup: initializing the browser and navigating to the home page.
- Test methods interact with different pages (e.g., LoginPage, FeedPage, PollSubmittionPage, VerifySubmittedPoll) to perform specific actions and fetch details.
- Assertions are used to validate the correctness of fetched poll details.
- Screenshots are taken and saved in case of an exception, providing a visual record of issues.
- Annotations (@BeforeMethod and @AfterMethod) help in setting up and tearing down the test environment before and after each test method.
  
####Conclusion:
This automation framework provides a robust solution for testing the auzmor platform, ensuring clean code, readability, and maintainability. The framework is designed to be platform-independent, supporting local and distributed testing using Selenium Grid. Follow the provided instructions in the README file to set up and execute the tests seamlessly.


