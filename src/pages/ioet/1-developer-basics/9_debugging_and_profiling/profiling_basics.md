---
layout: "../../../../layouts/BlogPost.astro"
title: "Profiling Basics"
pubDate: "2022-09-14"
---

## Author

- Daniela García @dsgarcia8

## Topics

- [Author](#author)
- [Topics](#topics)
- [What is performance profiling?](#what-is-performance-profiling)
- [Profiling tools](#profiling-tools)
  - [Cprofile (Python)](#cprofile-python)
    - [Example](#example)
    - [How to visualize cProfile reports?](#how-to-visualize-cprofile-reports)
    - [icicle](#icicle)
    - [Sunburst](#sunburst)
  - [Chrome profiling (Javacript)](#chrome-profiling-javacript)
    - [How to use the profiler tool in Chrome DevTools?](#how-to-use-the-profiler-tool-in-chrome-devtools)
    - [Visualiazing results](#visualiazing-results)
    - [Performance Flamechart](#performance-flamechart)
    - [Memory Area](#memory-area)
    - [Summary graph](#summary-graph)
  - [More profiling tools](#more-profiling-tools)

## What is performance profiling?

> Performance profilers are software development tools designed to help you analyze the performance of your applications and improve poorly performing sections of code. They provide measurements of how long a routine takes to execute, how often it is called, where it is called from, and how much of total time at some spot is spent executing that routine. [Fundamentals of Performance Profiling by SMARTBEAR](https://smartbear.com/learn/code-profiling/fundamentals-of-performance-profiling/)

## Profiling tools

### Cprofile (Python)

[cProfile](https://docs.python.org/3/library/profile.html) is an advanced library that  tracks functions to generate a list of the most often called functions. cProfile is beneficial to development because:

1. Provides  a standard library

2. Tracks different statistics call behavior

3. Developers  can use cProfile without restrictions

How to use cProfile ?

cProfile provides a simple run() function.

```Python
cProfile.run(statement, filename=None, sort=-1)
```

#### Example

[Read more](https://www.machinelearningplus.com/python/cprofile-how-to-profile-your-python-code/)

This python example adds elements to an array using a for loop in a range from 0 to 500000.

```Python
import cProfile

def create_array():
  arr=[]
  for i in range(0,500000):
    arr.append(i)

def print_statement():
  print('Array created successfully')


def main():
  create_array()
  print_statement()


if __name__ == '__main__':
    cProfile.run('main()')
```

We can observe the following result when running the code.

Output

Each column in the table means

- ncalls : Shows the number of calls made
- tottime: Total time taken by the given function. Note that the time made in calls to sub-functions are excluded.
- percall: Total time / No of calls. ( remainder is left out )
- cumtime: Unlike tottime, this includes time spent in this and all subfunctions that the higher-level function calls. It is most useful and is accurate for recursive functions.
- The percall following cumtime is calculated as the quotient of cumtime divided by primitive calls. The primitive calls include all the calls that were not included through recursion.
You could see that it isn’t very complex because the operation we did is simple.

```Python
Array created successfully
         500006 function calls in 0.111 seconds

   Ordered by: standard name

   ncalls  tottime  percall  cumtime  percall filename:lineno(function)
        1    0.000    0.000    0.111    0.111 <string>:1(<module>)
        1    0.003    0.003    0.111    0.111 test.py:12(main)
        1    0.066    0.066    0.108    0.108 test.py:3(create_array)
        1    0.000    0.000    0.000    0.000 test.py:8(print_statement)
   500000    0.030    0.000    0.030    0.000 {method 'append' of 'list' objects}
        1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
        1    0.012    0.012    0.012    0.012 {range}
```

#### How to visualize cProfile reports?

A best tool available at the moment for visualizing data obtained by cProfile module is [SnakeViz.](https://jiffyclub.github.io/snakeviz/)
SnakeViz has two visualization styles, icicle (the default) and sunburst.

#### icicle

> In the icicle visualization style functions are represented by rectangles. A root function is the top-most rectangle, with functions it calls below it, then the functions those call below them, and so on. The amount of time spent inside a function is represented by the width of the rectangle. A rectangle that stretches across most of the visualization represents a function that is taking up most of the time of its calling function, while a skinny rectangle represents a function that is using hardly any time at all.

![icicle](https://www.machinelearningplus.com/wp-content/uploads/2020/08/Screenshot-30-768x518.png)

#### Sunburst

> In the sunburst visualization style functions are represented as arcs. A root function is a circle at the middle, with functions it calls around, then the functions those functions call, and so on. The amount of time spent inside a function is represented by the angular extent of the arc (how far around the circle it goes). An arc that wraps most of the way around the circle represents a function that is taking up most of the time of its calling function, while a skinny arc represents a function that is using hardly any time at all.

![Sunburst](https://jiffyclub.github.io/snakeviz/img/sunburst.png)

### Chrome profiling (Javacript)

DevTools captures performance metrics as the page runs.

#### How to use the profiler tool in Chrome DevTools?

[Read more](https://yonatankra.com/how-to-profile-javascript-performance-in-the-browser/#Call_Tree)

1. Open the chrome browser with any website
2. Hit F12 OR right click on the screen and select “inspect element”
3. In the dev tools screen that opens, select the “Performance” tab
4. Click the “record” button. Now the app is being recorded
5. Once you are done recording, click on the “Stop” button to stop the recording
6. Check the recording’s result

#### Visualiazing results

In the following picture you can see everything that happened during the run.
![Results](https://lh4.googleusercontent.com/fPkQxS0NmYFl-hJo50S_ncbhVSsk4afmiGhansW8rkkEaj5Xy-8i-_Lu2D70bz_7tHe2GFUF_q_jPztx78Ok99SzmW4gghFRmf2TzpmtMSpix30u6cZGxXskAEJSAEHKHbOBAuXh)

On the results screen, there are several graphs and this might seem overwhelming when you view this screen for the first time. Below we will detail some of these graphs.

#### Performance Flamechart

> DevTools represents main thread activity with a flame chart. The x-axis represents the recording over time. The y-axis represents the call stack. The events on top cause the events below it. [Chrome devtools](https://developer.chrome.com/docs/devtools/evaluate-performance/reference/)

![Flamechart](https://lh5.googleusercontent.com/vlRDD1y0hj_yc9LZOKdGdJV0X9RQ9ZI-d7QfWNzd_TQdLW_53vUhgi40YxL0L76QtZsYMDv9_Nhuo8Qr2PxVi9EZa7xgWaMmnCQA-_abB-dWAxAnD34dh3k330IPfwnTLA_ngSsf)

#### Memory Area

The blue part is memory, red is document, green is DOM nodes, yellow is listeners and purple is GPU memory.  This part shows you trends in your app and can be useful when tracking down memory leaks.

![Memory Area](https://lh4.googleusercontent.com/Z618TX64s1uLka3UTYkYJTcfU2zou__cRETS6IJ8aOxOYjPC-3l9EUdw6_xX8l3TYM5eMnh9dUG_L9jaCR8s-mt9BWE1_LwbtTX9CmYUjTuiihnLaXZRo8KnvvETxkL2v64AaWuQ)

#### Summary graph

It shows you how much time was spent in the various lifecycles of the app

![Summary graph](https://lh4.googleusercontent.com/MINy5sNPcrhJnODCjPwp8okTYHZBw-zH4lcN1NhKxlvcdjwHMEpmTkyZRG3iPioa6XHOJhZ2WyUhI64we24dl7PPFmN8PTNLRfhlgXyeerhzlcflhXco5K225NtsOfPE0zBTDzjm)

### More profiling tools

- [Palanteer](https://github.com/dfeneyrou/palanteer): Palanteer can be used to profile both Python and C++ programs. Instrumenting Python applications is as simple as running the app through Palanteer, in the same way one uses cProfile. Function calls, exceptions, garbage collection, and OS-level memory allocations are all tracked.
- [Pyinstrument](https://github.com/joerick/pyinstrument): Pyinstrument works like cProfile in that it traces your program and generates reports about the code that is occupying most of its time. Pyinstrument’s reporting is more concise.
- [Py-spy](https://github.com/benfred/py-spy): Py-spy, like Pyinstrument, works by sampling the state of a program’s call stack at regular intervals, instead of trying to record every single call.
- [Firefox performance tools](https://firefox-source-docs.mozilla.org/devtools-user/performance/): The Performance tool gives you insight into your site’s general responsiveness, JavaScript and layout performance. With the Performance tool you create a recording, or profile, of your site over a period of time.
