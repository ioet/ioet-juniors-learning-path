---
layout: "../../../../layouts/BlogPost.astro"
title: "Linting"
---

In this guide you will learn about tools to help you improve your developer experience (DX).

## Authors

- Daniela García @dsgarcia8
- Jefferson Oña @jeffqev

## Topics

- [Authors](#authors)
- [Topics](#topics)
- [What is Linting?](#what-is-linting)
- [Why use Linting?](#why-use-linting)
  - [What all can linting help with?](#what-all-can-linting-help-with)
- [How lint tools work?](#how-lint-tools-work)
- [Example](#example)
- [Code linters tools](#code-linters-tools)
- [Visual Studio Code linter extensions](#visual-studio-code-linter-extensions)
  - [ESlint](#eslint)
  - [Pylint](#pylint)
- [References](#references)

## What is Linting?

> Linting is the automated checking of your source code for programmatic and stylistic errors. This is done by using a lint tool (linter). A lint tool is a basic static code analyzer. [Read more](https://www.perforce.com/blog/qac/what-lint-code-and-why-linting-important)

## Why use Linting?

As individual developer Linting is important to reduce errors and improve the overall quality of your code. Using lint tools can help you accelerate development and reduce costs by finding errors earlier. As a developer team each developer has his own way of programming but using lint this can be standardized and make code looks like written by a single person

[more reasons to use lint in a team](https://sourcelevel.io/blog/what-is-a-linter-and-why-your-team-should-use-it)

### What all can linting help with?

- Flagging bugs in your code from syntax errors
- Giving you warnings when code may not be intuitive
- Providing suggestions for common best practices
- Keeping track of TODO’s and FIXME’s
- Keeping a consistent code style

## How lint tools work?

Here’s how lint tools are typically fit into the development process.

1. Write the code.
2. Compile it.
3. Analyze it with the linter.
4. Review the bugs identified by the tool.
5. Make changes to the code to resolve the bugs.
6. Link modules once the code is clean.
7. Analyze them with the linter.
8. Do manual code reviews.

## Example

to give an example in javascript having the following code

``` javascript
const test = 'I am a test';
console.log(`Test: ${test}`);
const test = 'Another one.';
```

the constant test is declared twice so the linter can identify before execution

``` text
  10:9  error  Parsing error: Identifier 'test' has already been declared

   8 |   const test = 'I am a test';
   9 |   console.log(`Test: ${2}`);
> 10 |   const test = 'Another one.';
     |         ^
```

## Code linters tools

Linter helps to ensure that your code does not include any structural issues which can make your code harder to maintain.

Linters are available for most programming languages. Here are the most common ones:

| Programming Language | Linter|
| ------ | ------ |
| JavaScript | [ESlint](https://github.com/eslint/eslint)|
| Python | [Pylint](https://pylint.pycqa.org/en/latest/) |
| Java | [Checktyle](https://checkstyle.org/)|
| Ruby |[rubocop](https://github.com/rubocop/rubocop) |
| Go | [golangci-lint](https://github.com/golangci/golangci-lint) |
| C/C++| [clang-format](https://clang.llvm.org/docs/ClangFormat.html) |
| Rust | [rust-clippy](https://github.com/rust-lang/rust-clippy) |
| Swift | [SwiftLint](https://github.com/realm/SwiftLint) |

For more information and tools check [Awesome linters](https://github.com/caramelomartins/awesome-linters#go)

## Visual Studio Code linter extensions

Visual Studio Code is one of the most popular code editors used by software developers. While it has many great features built-in, there are a lot of extensions you can install to increase your productivity.

Text editors show you in real time linting errors when installing extensions,
for example in the following image you can see how the ESlint extension shows the developer the errors.

![ESlint](https://debug.to/?qa=blob&qa_blobid=3301089410252071586)

### ESlint

[VS Code ESlint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint): uses the ESLint library installed in the opened workspace folder.

If you haven't installed ESLint either locally or globally do so by running:

```bash
 npm install -g eslint
```

### Pylint

[Pylint extension for Visual Studio Code](https://github.com/microsoft/vscode-pylint): Once installed in Visual Studio Code, pylint will be automatically executed when you open a Python file.

## References

- [What is a linter and why your team should use it?](https://sourcelevel.io/blog/what-is-a-linter-and-why-your-team-should-use-it)
- [What Is Lint Code? And Why Is Linting Important?](https://www.perforce.com/blog/qac/what-lint-code-and-why-linting-important)
- [Linting](https://developerexperience.io/practices/linting)
