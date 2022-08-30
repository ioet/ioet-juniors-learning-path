# Manual testing

## Authors

- Daniela García @dsgarcia8

## Topics

- [What is manual testing?](#what-is-manual-testing)
- [Why we need manual testing?](#why-we-need-manual-testing)
- [Advantages of manual testing](#advantages-of-manual-testing)
- [Disadvantages of manual testing](#disadvantages-of-manual-testing)
- [Types of manual testing](#types-of-manual-testing)
  - [Acceptance Testing](#acceptance-testing)
  - [Black Box Testing](#black-box-testing)
  - [Integration Testing](#integration-testing)
  - [System testing](#system-testing)
  - [Unit Testing](#unit-testing)
  - [White Box Testing](#white-box-testing)
- [Manual Testing Steps](#manual-testing-steps)
- [Why combine manual and automated tests?](#why-combine-manual-and-automated-tests)
  - [Challenges of Managing Manual & Automated Testing Together](#challenges-of-managing-manual--automated-testing-together)
- [References and Additional Resources](#references-and-additional-resources)

## What is manual testing?

Manual software testing is when human testers check the quality of a new application without the use of automation tools or scripting. The goal is to identify bugs or defects, ensure the product is error-free, and ensure it meets the specified functional requirements.

## Why we need manual testing?

Whenever a new program enters the market and is unstable, contains bugs, causes problems, or causes issues for consumers.

If we don't want to run into issues like this, we should run the program through one round of testing to make it stable and bug-free before delivering it to the client. If the application is bug-free, the end user will find it easier to use.

The test engineer may test the application from the standpoint of the end user and become more familiar with the product if they conduct manual testing. This allows them to design accurate test cases for the application and provide timely feedback on it.

## Advantages of manual testing

- Uses human intelligence to find errors
- Lets testers focus on complex features and functions
- Tester knowledge of the project
- Detects errors outside of the code
- Provides accurate emulation of user experience
- It helps maintain a testable system

## Disadvantages of manual testing

- It requires more time than automated testing
- It is susceptible to human errors
- It is time-consuming to maintain test cases
- Testers need to know the product well
- It is costly to maintain manual testers

## Types of manual testing

### Acceptance Testing

This is a method of testing the internal structures or workings of an application that is also known as transparent box testing or structural testing. It is carried out by the developer, who checks the internal codes of the software before passing it to a test engineer.

### Black Box Testing

This method, also known as behavioral testing, aims to analyze an application's functionality from the end-point user's of view. Because the internal code structure is not visible during testing (hence the name "Black Box"), testers are only aware of the software's inputs and expected outputs.

### Integration Testing

The process of testing an application with two or more integrating components is known as integration testing. It is carried out after the individual components have been unit-tested and aims to identify issues with the interfaces and their interactions.

### System testing

System testing entails testing the entire system after all of its components have been unit-tested and integrated. It validates that the entire application works as intended by comparing it to the original requirements.

### Unit Testing

To ensure that each function works as intended, the various units or components that make up an application's source code are tested at this point. Due of the thorough knowledge of the internal program architecture and code required, developers typically handle it rather than engineers.

### White Box Testing

This technique for testing an application's interior workings or structures is often referred to as structural testing or transparent box testing. It is carried out by the developer, who examines the internal codes of the software before handing it off to a test engineer.

## Manual Testing Steps

1. Requirement Gathering
2. Sharing and Discussion
3. Test Environment and Resources Setup
4. Creating Test Scenarios and Test Cases
5. Test Execution and Defect Reporting
6. Defect Retesting and Closure
7. Feedback and Recommendation
8. Product Release, Test Cases and Repository Maintenance
9. Updating test cases

## Why combine manual and automated tests?

> Automated testing usually enhances testing speed and consistency, but it is only as good as the scripts you wrote. [PractiTest](https://www.practitest.com/qa-learningcenter/best-practices/coordinate-automated-and-manual-testing/#:~:text=When%20the%20combination%20is%20successful,as%20the%20scripts%20you%20wrote.)

Although technology saves time, manual testing is still an essential component of software development. Human testers are able to create numerous test scenarios for an application or function and think like an end user.

It's important to keep in mind that, despite software testing's best efforts, it is practically impossible to find every possible flaw. Manual testers frequently catch problems that a machine might miss, but they are also prone to human error.

### Challenges of Managing Manual & Automated Testing Together

- Very different entities: While manual testing are typically longer and less specified, automated tests are typically deeper and more focused. Both test types are different from one another.
- Different scale of tests and runs: Typically, there are a lot more automated tests than manual tests, especially when unit tests are included. Additionally, there are many more automated runs than manual ones because they are always in use (sometimes daily or continually).
- Different timelines for results: While manual results may take hours or days to complete, automated tests can complete full cycles in minutes or hours.
- Different approach to analyse results: Manual run "fails" typically indicate bugs, and there appears to be some relationship between the quantity of failed tests and the quantity of bugs discovered. Automated tests typically fail much more frequently than they find defects, and they contain a great deal more false negatives than true positives.

## References and Additional Resources

- [Manual Testing - what is it?](https://www.globalapptesting.com/manual-testing-best-practices)
- [How to coordinate your automated and manual testing](https://www.practitest.com/qa-learningcenter/best-practices/coordinate-automated-and-manual-testing/#:~:text=When%20the%20combination%20is%20successful,as%20the%20scripts%20you%20wrote.)
- [Manual Testing Tutorial for Beginners](https://mindmajix.com/manual-testing-tutorial)
- [Manual Testing Tutorial: What is, Types, Concepts](https://www.guru99.com/manual-testing.html)
- [Manual Testing for Beginners](https://www.browserstack.com/guide/manual-testing-tutorial)
