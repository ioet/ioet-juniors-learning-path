# Makefile

Stop repeating terminal commands over and over again and automate them using makefile

## Author

- Jefferson Oña @jeffqev

## Topics

- [What is Makefile](#what-is-makefile)
- [Why would we use Makefile](#why-would-we-use-makefile)
- [Hello World using Makefile](#hello-world-using-makefile)
- [Makefile basics](#makefile-basics)
  - [Syntax](#syntax)
  - [Variables](#variables)
  - [Target prerequisites](#target-prerequisites)
- [Makefile Topics](#makefile-topics)

## What is Makefile?

Makefile is a special file, containing shell commands, that you create and name makefile.  [What is a Makefile?](https://www.sis.pitt.edu/mbsclass/tutorial/advanced/makefile/whatis.htm)

## Why would we use Makefile?

The normal way to run commands involves repetition and can easily be mistyped, especially when the commands get longer and more numerous, and more dependencies show up. Creating a makefile means that all one needs to do at the very least is run make, followed optionally by make install.

``` makefile
install:
    sudo a_super_long_command_with_several_parameters -o any_option
```

with a makefile you will only execute `make install` instead `a_super_long_command_with_several_parameters`

## Hello World using Makefile

Create a file with name Makefile in a directory with following content:

``` makefile
say_hello:
    echo Hello World
```

Now run the file by typing `make say_hello`:

``` shell
$ make say_hello
echo Hello World
Hello World
```

## Makefile basics

### Syntax

``` makefile
targets: prerequisites
    command
    command
    command
```

- The targets: are file names, separated by spaces. Typically, there is only one per rule.
- The commands: are a series of steps typically used to make the target(s). These need to start with a tab character, not spaces.
- The prerequisites: are also file names, separated by spaces. These files need to exist before the commands for the target are run. These are also called dependencies

> Note if you want a default target you can name it `all` and just execute `make` in the terminal

### Variables

Variables are strings and you can assign with "=" or ":="

```makefile
file = main.py

all:
    python $(file)
```

> Note: also you can execute variables environment variables using `$$any_variable`

More about variables in makefile in [makefile tutorial - variables](https://makefiletutorial.com/#variables-pt-2)

### Target prerequisites

If you want to execute several targets, you can write on the prerequisites of a target and execute all of them at the same time.

``` makefile
all: install build run

install:
    echo install
build:
    echo build
run:
    echo run
```

## Makefile Topics

1. [Targets](https://makefiletutorial.com/#targets)
2. [Automatic Variables and Wildcards](https://makefiletutorial.com/#automatic-variables-and-wildcards)
3. [Fancy Rules](https://makefiletutorial.com/#fancy-rules)
4. [Commands and execution](https://makefiletutorial.com/#commands-and-execution)
5. [Variables](https://makefiletutorial.com/#variables-pt-2)
6. [Conditional](https://makefiletutorial.com/#conditional-part-of-makefiles)
7. [Functions](https://makefiletutorial.com/#functions)
8. [Other Features](https://makefiletutorial.com/#other-features)

## References

- [Makefile tutorial](https://makefiletutorial.com/)
- [What is a Makefile?](https://www.sis.pitt.edu/mbsclass/tutorial/advanced/makefile/whatis.htm)