---
layout: "../../../../layouts/BlogPost.astro"
title: "Functional testing"
pubDate: "2022-09-14"
---

## Contributors

- [Daniela Garcia](https://github.com/dsgarcia8)

## Content

- [Contributors](#contributors)
- [Content](#content)
  - [What is functional testing?](#what-is-functional-testing)
  - [Brief introduction to software testing](#brief-introduction-to-software-testing)
    - [Functional testing vs Non-functional testing](#functional-testing-vs-non-functional-testing)
    - [Some examples of functional testing](#some-examples-of-functional-testing)
    - [Some examples of non-functional testing](#some-examples-of-non-functional-testing)
  - [Functional Testing Best Practices](#functional-testing-best-practices)
  - [What do you test in Functional Testing?](#what-do-you-test-in-functional-testing)
  - [How to do Functional Testing?](#how-to-do-functional-testing)
  - [Functional Testing Tools](#functional-testing-tools)
- [References and Additional Resources](#references-and-additional-resources)

### What is functional testing?

FUNCTIONAL TESTING is a sort of software testing in which the software system is validated against functional requirements/specifications. The goal of functional testing is to test each function of a software program by giving adequate input and comparing the output to the Functional requirements.

Functional testing is primarily concerned with black box testing and is unconcerned with the application's source code. This testing examines the Application Under Test's User Interface, APIs, Database, Security, Client/Server connection, and other features. Testing can be performed manually or automatically.

### Brief introduction to software testing

A crucial step in application lifecycle management's quality assurance process is software testing, whether it be manual or automated. It helps determine whether a system complies with the specified project requirements for testers, developers, IT operations, project owners, business analysts, and end users.
These tests fall into two broad categories: functional testing and non-functional testing.

#### Functional testing vs Non-functional testing

Functional Testing    | Non-Functional Testing          |
-----------:|--------------:|
Functional testing validates the system against the functional requirements using the functional specification provided by the client.    | Non-functional testing examines the software system's performance, reliability, scalability, and other non-functional features.          |
Functional testing is executed first   | Functional testing is executed first Non-functional testing should be performed after functional testing
Manual Testing or automation tools can be used for functional testing     | Using tools will be effective for this testing        |
Business requirements are the inputs to functional testing      | Performance parameters like speed, scalability are inputs to non-functional testing.      |
Functional testing describes what the product does | Nonfunctional testing describes how good the product works
Easy to do Manual Testing | Tough to do Manual Testing

#### Some examples of functional testing

- Smoke Testing
- Sanity Testing
- Unit Testing
- Integration Testing
- Regression Testing
- Localization Testing
- User Acceptance Testing  

#### Some examples of non-functional testing

- Performance Testing
- Usability Testing
- Security Testing
- Volume Testing
- Scalability Testing
- Load Testing
- Stress Testing
- Recovery Testing
- Configuration Testing

You can read more about these tests in [Micro Focus Community](https://community.microfocus.com/adtd/b/sws-alm/posts/types-of-software-testing-functional-non-functional)

### Functional Testing Best Practices

- Create Test Cases Early: Do not wait until application or module code is complete before beginning to create test cases. User requirements will be most fresh at the early stages of the project. You can always change test cases later if necessary.
- Automate: Functional testing can be a difficult, time-consuming, and repetitive procedure. The more you automate, the faster you can verify expected functionality or find and rectify errors, as well as save time and money on testing. It may not be possible, or even desired, to automate all test cases, but even removing the most critical test cases from the manual list will significantly increase your test ROI.
- Understand the User’s Thought Process: Functional testers must have a thorough understanding of the end user's cognitive process. Each application frequently has a variety of users (buyers, sellers, administrators, data entry clerks, supervisors, etc.). Each test strategy must take into account the various sorts of users and their normal application navigation.
- Prioritize: Time and resources are limited for testers. Every feature cannot be tested. Some application functions are high-priority and must thus be tested before lower-priority features.

### What do you test in Functional Testing?

The primary goal of functional testing is to ensure that the software system functions properly. It mostly focuses on:

- Mainline functions: A test of an application's primary functions.
- Basic Usability: It entails testing the system's basic usability. It determines whether or not a user can freely navigate through the screens without difficulty.
- Accessibility: Examines the system's usability for the user.
- Error Conditions: The use of testing techniques to detect errors. It determines whether appropriate error messages are presented.

### How to do Functional Testing?

The following is a step-by-step procedure for performing Functional Testing:

- Recognize the Functional Requirements
- Based on the criteria, identify test input or test data.
- Calculate the expected results using the test input values you've chosen.
- Carry out test cases
- Compare the actual and predicted results.

### Functional Testing Tools

- [Selenium](https://www.selenium.dev/) – Popular Open Source Functional Testing Tool
- [QTP](https://www.tutorialspoint.com/qtp/index.htm) – Very user-friendly Functional Test tool by HP
- [JUnit](https://www.guru99.com/junit-tutorial.html)– Used mainly for Java applications and this can be used in Unit and System Testing
- [soapUI](https://www.soapui.org/) – This is an open source functional testing tool, mainly used for Web service testing. It supports multiple protocols such as HTTP, SOAP, and JDBC.

## References and Additional Resources

- [What is Functional Testing? Types & Examples (Complete Tutorial)](https://www.guru99.com/functional-testing.html)
- [Functional Testing Vs Non-Functional Testing](https://www.softwaretestinghelp.com/functional-testing-vs-non-functional-testing/)
- [Complete Functional Testing Guide With Its Types And Example](https://www.softwaretestinghelp.com/guide-to-functional-testing/)
- [Functional Testing : A Detailed Guide](https://www.browserstack.com/guide/functional-testing)
- [Functional testing](https://www.techtarget.com/searchsoftwarequality/definition/functional-testing)
