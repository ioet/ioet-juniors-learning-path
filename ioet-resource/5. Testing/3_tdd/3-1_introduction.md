# TDD Introduction

## Contributors

- [Josué Cando](https://github.com/JosueOb)

## Content

- [TDD](#tdd-introduction)
  - [Contributors](#contributors)
  - [Content](#content)
  - [Introduction](#introduction)
    - [General Steps](#general-steps)
    - [Technical Documentation](#technical-documentation)
    - [Benefits](#benefits)
    - [Disadvantages](#disadvantages)
    - [Frameworks](#frameworks)
  - [Conclusions](#conclusions)
  - [References](#references)

## Introduction

TDD - test-driven development, also called test-driven design, is a software programming
implementation method that weaves unit testing, programming and refactoring into the source code.

It was introduced as part of a broader software design paradigm known as Extreme Programming (XP),
which is part of the agile software development methodology.

In TDD, developers start creating small test cases for each feature based on their initial
understanding. The main intention of this technique is to modify or write new code only if tests
fail. This avoids duplication of test scripts.

### General Steps

1. The first step is to quickly add a test, basically just enough code to fail.
2. Once a test fails, developers have to make the minimal changes necessary to correct the code so
   that it can run successfully when it is run again.
3. Once the test runs successfully, check for redundancy or any possible code optimizations to
   enhance overall performance. Ensure that refactoring does not affect the external behavior of the
   program.

![TDD process](https://www.agilest.org/wp-content/uploads/2016/10/tdd-fig-2@2x-8.png)

### Technical Documentation

Most programmers do not read the written documentation of a system or app, but prefer to work with
the code, and there’s nothing wrong with this. But in this case, well-written tests are very useful
technical documentation.

### Benefits

- Provide a functional, modular and simple code.
- Improve team productivity.
- Meet all customer requirements.
- Nearly zero defects.
- Shorter development cycles.
- Have a high code coverage rate.
- Have a good technical documentation.

### Disadvantages

- Writing tests before writing code means that you need to know the software requirements and code
  specification before you start coding the solution. In large projects already started,
  understanding the requirements and specification becomes time-consuming and sometimes complicated.

### Frameworks

Based on single programming languages, there are multiple frameworks that support test-driven
development. Some of the most popular ones are listed below:

- [JUnit](https://junit.org/junit5/docs/current/user-guide/) or [TestNG](https://testng.org/doc/)
  for unit tests in Java.
- [Mocha](https://mochajs.org/) or [Jest](https://jestjs.io/) for TDD in JavaScript.
- [Pytest](https://docs.pytest.org/en/7.1.x/) for TDD in Python.
- [Mockito](https://site.mockito.org/) for Rest API testing.
- [Selenium](https://www.selenium.dev/documentation/) for test automation.
- [WebdriverIO](https://webdriver.io/docs/what-is-webdriverio/) for progressive automation.
- [csUnit](http://csunit.org/) and [NUnit](https://nunit.org/) for TDD in .NET projects.
- [Rspec](https://rspec.info/) for TDD in Ruby projects

## Conclusions

- The testing process drives software development.
- Test-driven development designs better, more risk-tolerant code.
- When TDD programming is used, the code becomes clearer and easier to understand.
- The benefit of TDD is largely attributed to code reuse and the ability to easily refactor code.

## References

- [5 Steps of test-driven development](https://developer.ibm.com/articles/5-steps-of-test-driven-development/)
- [Test-driven Development Frameworks You Must Know](https://www.nan-labs.com/blog/test-driven-development-examples-framework/)
- [What strategies work best for adopting TDD](https://codeit.us/blog/test-driven-development#:~:text=While%20the%20traditional%20coding%20process%20starts%20with%20the,starting%20with%20writing%20a%20test%202%20checking%20it)
