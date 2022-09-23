---
layout: "../../../../layouts/BlogPost.astro"
title: "Debugging"
---

## Authors

- Daniela García @dsgarcia8
- Jefferson Oña @jeffqev

### What is Debugging?

> Debugging is a computer programing process for finding and resolving errors in software or a website, often referred to as "bugs." [More info.](https://www.indeed.com/career-advice/career-development/debugging#:~:text=Debugging%20is%20important%20because%20it,error%20affects%20a%20program%20overall.)

### Why we need to Debug?

> As developers, no matter how good we get, we're going to spend countless hours debugging our code, so we should try to get better and quicker at it. [Why should you learn about debugging ?](https://www.freecodecamp.org/news/what-is-debugging-how-to-debug-code/#whyshouldyoulearnaboutdebugging)

- Debugging makes you a better learner, the practice of detecting the errors made in your written code and correcting them offers an opportunity to learn new tricks and skills to help you debug faster in the future.
- Debugging  allows earlier detection of an error and makes the process of software development stress-free and unproblematic.
- Performing debugging at the initial stage saves the time of software developers as they can avoid the use of complex codes in software development. It not only saves the time of software developers but also saves their energy.
- It provides easy interpretations by providing more information about data structures
Release bug-free software: By finding errors in software, it allows developers to fix them before releasing them and provides bug-free software to the customers.

### Debugging in Visual Studio Code

#### Configurations

- [Python](https://code.visualstudio.com/docs/python/debugging)
- [Node](https://code.visualstudio.com/docs/nodejs/nodejs-debugging)
- [Browser debugging in VS Code](https://code.visualstudio.com/docs/nodejs/browser-debugging)

#### Breakpoints

Breakpoints are temporary markers that you place in your executable program to tell the debugger to stop your program at a given point. You set breakpoints wherever you want to pause debugger execution.

![Breakpoint](https://code.visualstudio.com/assets/docs/editor/debugging/bpts-in-overview.png)

#### Data inspection

Variables

The VARIABLES pane is where you can inspect the values of variables and expressions that were evaluated at the breakpoint.

You can perform the following actions

- Set Value lets you modify the variable's value to test certain values while code is executing.
- Copy Value copies the value of a variable to the clipboard
- Copy as Expression copies an expression to access the variable
- Add to Watch adds the variable to the WATCH pane for monitoring

![Variables](https://blog.logrocket.com/wp-content/uploads/2021/06/Inspecting-values-VARIABLES-WATCH-Pane-1.png)

Watch

The main benefit of the WATCH pane is that you can easily bring values that you want to monitor into view while the code is paused.

Instead of digging through a deeply nested property in the VARIABLES pane each time you want to check its value, you can add it to the WATCH pane for easy access. This is most useful when determining the values of several variables at once since they are automatically recalculated in the execution.

![Watch](https://blog.logrocket.com/wp-content/uploads/2021/06/Watch-pane.png)

#### Debug Console

Expressions can be evaluated in the Debug Console. To open the Debug Console use the Open Console action at the top of the Debug pane or using the Command Palette.

![Debug Console](https://code.visualstudio.com/assets/docs/editor/debugging/debugconsole.png)

#### Debugging with docker

When you want to do remote debugging from a docker container you have to expose a port which you are going to attach to vscode debugger

For example in js you could be run

```shell
docker run -it --rm -p 9229:9229 -v "$(pwd):/usr/src/app" -w "/usr/src/app" node:16.13.1 node --inspect-brk=0.0.0.0 main.js
```

and in the debug configuration you can add the port to which it is going to access

``` Json
{
    "name": "Attach",
    "port": 9229,
    "request": "attach",
    "skipFiles": [
        "<node_internals>/**"
    ],
    "type": "node"
},
```

#### More info

- [Debugging in Visual Studio Code](https://code.visualstudio.com/docs/editor/debugging)
- [Debugging feature tutorial](https://www.microsoft.com/videoplayer/embed/RWAIIi)
- [How to debug Node.js apps in Visual Studio Code](https://blog.logrocket.com/how-to-debug-node-js-apps-in-visual-studio-code/)
- [How to debug containerized apps](https://code.visualstudio.com/docs/containers/debug-common)
