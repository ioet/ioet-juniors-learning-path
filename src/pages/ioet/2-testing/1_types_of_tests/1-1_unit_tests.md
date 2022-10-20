---
layout: "../../../../layouts/BlogPost.astro"
title: "Unit tests"
pubDate: "2022-09-14"
---

## Contributors

- [Daniela Garcia](https://github.com/dsgarcia8)
- [Jean Carlos Alarcón](https://github.com/jcalarcon98)

## Content

- [Contributors](#contributors)
- [Content](#content)
  - [What is Unit Testing](#what-is-unit-testing)
  - [What makes a good unit test](#what-makes-a-good-unit-test)
  - [Unit testing Best Practices](#unit-testing-best-practices)
    - [Naming your tests](#naming-your-tests)
    - [Arranging your tests](#arranging-your-tests)
    - [Avoid login in tests](#avoid-logic-in-tests)
    - [Avoid multiple acts](#avoid-multiple-acts)
  - [Additional Resources for Unit Testing](#additional-resources-for-unit-testing)

### What is Unit Testing?

A unit test is a way of testing the smallest piece of code. In most programming languages, it could be a function, subroutine, method or property. This way of testing allow us to verify if our code is working as expected. It's called **unit testing** because you break down the functionality of your solution into discrete testable behaviors that you can test as individual units.

Unit testing has the greatest effect on the quality of your code when it's an integral part of your software development workflow. As soon as you write a function or other block of application code, create unit tests that verify the behavior of the code in response to standard, boundary, and incorrect cases of input data, and that check any explicit or implicit assumptions made by the code

### What makes a good unit test?

Unit testing principles demand that a good test is:

- Easy to write
- Readable
- Reliable
- Fast
- Truly unit, not integration

### Unit testing Best Practices

#### Naming your tests

Naming standards are important because they explicitly express the intent of the test.

- The name of the method being tested.
- The scenario under which it's being tested.
- The expected behavior when the scenario is invoked.

**Example**

```python
# Bad

def test_one():
    pass
```

```python
# Better

def test_add_single_number_should_return_same_number():
    pass
```

#### Arranging your tests

**Arrange**, **Act**, **Assert** is a common pattern when unit testing. As the name implies, it consists of three main actions:

- Arrange your objects, creating and setting them up as necessary.
- Act on an object.
- Assert that something is as expected.

It allow us to clearly separates what is being tested from the arrange and assert steps. This pattern also increases readability, one of the most important aspects when writing a test. Separating each of these actions within the test clearly highlight the dependencies required to call your code, how your code is being called, and what you are trying to assert.

**Example**

```python
# Bad

def test_add_empty_string_should_return_zero():
  # Arrange
  string_calculator = StringCalculator()
  
  # Assert
  assert string_calculator.add('') == 0

```

```python
# Better

def test_add_empty_string_should_return_zero():
  # Arrange
  string_calculator = StringCalculator()

  # Act
  result = string_calculator.add('')

  # Assert
  assert result == 0

```

#### Avoid logic in tests

When writing your unit tests avoid manual string concatenation and logical conditions such as `if`, `while`, `for`, `switch`, etc, because you need to focus on the end result, rather than implementation details also there is less chance to introduce a bug inside of your tests.

#### Avoid multiple acts

When writing your tests, try to only include one Act scenario per test. Common approaches to using only one act include:

- Create a separate test for each act.
- Use parameterized tests.

**Why?**

- When the test fails it is not clear which Act is failing.
- Ensures the test is focussed on just a single case.
- Gives you the entire picture as to why your tests are failing.

### Additional Resources for Unit Testing

- [JavaScript Unit Testing Guide](https://github.com/mawrkus/js-unit-testing-guide)
- [Unit testing tips by examples in PHP](https://github.com/sarven/unit-testing-tips)
- [Angular Testing Course](https://github.com/angular-university/angular-testing-course)
- [Unit Testing best practices with .NET](https://docs.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices)
