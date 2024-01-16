# PROJECT TITLE: Auzmor UI Automation Framework

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

## LINK: [Auzmor Application](https://office-qa.auzmor.com/login)

### Credentials:
- Username: dohutoja.ohabufi@jollyfree.com
- Password: Password1@

## OVERVIEW:

This repository contains an automated testing framework designed for the Auzmor application. The framework aims to provide a scalable, maintainable, and platform-independent solution for testing the creation and submission of polls in the social feed.

## PREREQUISITES:

Before running the tests, ensure you have the following installed:

Java Development Kit (JDK)
Maven
Selenium
TestNG
Chrome Browser

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

- **src/main/java/BaseTest:** BaseTest contains the BaseClass with common methods for navigating and interacting with the application.

- **src/main/java/PageObjects:** It contains all the page classes representing different pages of the Social Feed application.
  - **/FeedPage:** Page class for interacting with the Social Feed.
  - **/LoginPage:** Page class for logging into the Auzmor website.
  - **/PollCreationPage:** Page class for creating and submitting polls.
  - **/VerifySubmittedPollPage:** Page class for verifying the submitted poll.

- **src/main/java/Utilities:** Utility classes for handling common functionalities.
  - **/ReadPropertiesFile:** Reads configuration properties from the config.properties file.
  - **/UtilityFile:** Handles screenshot functionalities.

- **src/test/java/SocialFeedTest:** Test class implementing scenarios for social feed automation.
  - **/PollCreationTest:** Test class for creating and submitting polls.

- **pom.xml:** It contains configuration information related to the project's build process, dependencies, plugins, and other settings.

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

1. Open the application and navigate to the Social Feed.
2. Click on the "Feed" tab.
3. Initiate a new post by clicking on the "What’s on your mind" section.
4. Add content to the post.
5. Click on the "Polls" CTA to create a poll.
6. Enter a relevant poll question.
7. Add at least two poll options.
8. Select a poll duration.
9. Click on the "Add a poll" button.

### TEST CASE-2 (Submit Poll and Verify Visibility):

10. Click on the "Submit Post" button to publish the poll.
11. Return to the Social Feed.
12. Check if the submitted poll is visible on the feed page.

### TEST CASE-3 (Additional Verifications):

13. Verify that the poll cannot be submitted without a valid question.
14. Verify that the poll cannot be submitted with insufficient options.
15. Check if the submitted poll is visible on the feed page.


