# Integration tests

## Authors

- Daniela García @dsgarcia8
- Jean Carlos Alarcón @jcalarcon98

## Topics

- [What is integration testing?](#what-is-integration-testing)
- [When to use it?](#when-to-use-it)
- [Advantages](#advantages)
- [Integration test example](#integration-test-example)
- [Integration testing tools](#integration-testing-tools)
- [References](#references)

## What is integration testing?

> Is a type of software testing in which the different units, modules or components of a software application are tested as a combined entity. [More info](https://www.techtarget.com/searchsoftwarequality/definition/integration-testing#:~:text=Integration%20testing%20%2D%2D%20also%20known,be%20coded%20by%20different%20programmers.)

When doing integration testing, several application components are joined and their behavior is evaluated as a whole. After integration, it's crucial to check that each unit is operating as planned and communicates effectively with one another.

## When to Use it?

The Test Pyramid, a way of thinking about tests that suggests giving priority to quick unit tests over slower types of testing, must be taken into consideration in order to comprehend when to apply which approach.

![test pyramid](https://lh5.googleusercontent.com/NvG3ZlgXwFjpvJEu1vjaj283AI4C3X_kVvPpMB5tVjvMWkK9wSAefDRtObfwXWu0ADAotHsQG_aFAFRwD6RFO_9QvMdTKI1UCc86atHqDU-bgokMOAx7TJwqVPwivERTY6-huOoj)

## Advantages

This testing has many benefits, some of which are stated below.

- Through this testing, the functionality of the integrated modules and components is confirmed.
- Integration testing can be started once the modules to be tested are available.
- It does not require the other module to be completed for testing to be done, as Stubs and Drivers can be used for the same.
- It recognizes interface-related faults.

## Integration test example

Let's look at an example of Integration Testing. Assume you work for an IT business that has been tasked with developing an online shopping website for Gold World, a jewelry company.

![example](https://cdn.dribbble.com/users/324533/screenshots/1419546/e-commerce.gif)

Following the completion of requirements collecting, analysis, and design, one developer was assigned to develop each of the modules listed below.

- User registration and Authentication/Login
- Product Catalogue
- Shopping Cart
- Billing
- Payment Gateway Integration
- Shipping and Package Tracking

After assigning each module to a developer, the developers began creating the functionality on their own machines. As they worked on constructing the module, they deployed their respectives modules on their own machines to determine what worked and what didn't.

After finishing development, the developers tested their individual functionalities as part of their unit testing and discovered certain flaws. They fixed these flaws. They thought their modules were finished at this time.

The QA Manager proposed that integration testing be performed to ensure that all modules function properly.

When they deployed all the app, they discovered that the program did not function properly since the separate modules did not operate well together. There were issues, such as the user's shopping cart not showing things added earlier after logging in, the bill amount not including shipping fee, and so on.

As a result, Integration Testing assists us in identifying, resolving, and ensuring that the program as a whole operates as planned.

## Integration testing tools

- Jasmine: is a behavioral driven development (BDD) framework. Using this tool tests can be run in isolation. Jasmine tool supports various browsers like Chrome, Internet Explorer, Safari, Firefox etc. It suits for websites where JavaScript runs. It has clean and simple syntax so that one can easily write tests. [Jasmine](https://jasmine.github.io/)
- FitNesse: an open-source project that supports all major languages, highly adaptable, and doesn’t require an additional installation. [Fitnesse](http://docs.fitnesse.org/FrontPage)
- VectorCAST: simple and transparent technology used for testing important business systems. [VectorCAST](https://www.vector.com/int/en/products/products-a-z/software/vectorcast/)
- Selenium: is a large-scale open-source project that offers several solutions for test automation. It is used mostly for web applications, and you can run integration testing using Selenium. [Selenium](https://www.selenium.dev/)
- Pytest: Pytest is the main testing environment for Python, which is widely used for writing and running test code. It is easy to write small tests using Pytest, while it can also scale up and works perfectly for testing complex applications and libraries. [Pytest](https://docs.pytest.org/en/7.1.x/)

Read more about [Integration Testing Tools and Practices to Start Using Today](https://u-tor.com/topic/start-integration-testing-today)

## References

- [What is integration testing? The basics explained!](https://u-tor.com/topic/integration-testing)
- [What Is Integration Testing (Tutorial With Integration Testing Example)](https://www.softwaretestinghelp.com/what-is-integration-testing/)
- [What is Integration testing? Examples, How To Do, Types/Approaches, Differences
](http://tryqa.com/what-is-integration-testing/)
- [Unit Test vs. Integration Test: Tell Them Apart and Use Both](https://www.testim.io/blog/unit-test-vs-integration-test/#integration-test)
