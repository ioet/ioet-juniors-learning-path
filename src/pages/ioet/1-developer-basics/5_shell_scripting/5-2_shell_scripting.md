---
layout: "../../../../layouts/BlogPost.astro"
title: "Shell Scripting"
pubDate: "2022-09-14"
---

## Contributor

- [Jipson Murillo](https://github.com/Jobzi)

![Shell](https://miro.medium.com/max/1162/0*SuLFBZ0FTHLh1mp5.png)

You might have came across the word ‘script’ a lot of times, but what is the meaning of a script? Basically, a script is a program that contains a series of commands to be executed. These commands are executed by an interpreter. Anything you can put into a command line, you can put in a script. And, scripts are great for automating tasks.  
If you find yourself repeating some commands frequently, you can, rather you should, create a script for doing it!

## Content

- [Contributor](#contributor)
- [Content](#content)
- [¿What is CLI and GUI?](#what-is-cli-and-gui)
- [¿Why would we use CLI over GUI?](#why-would-we-use-cli-over-gui)
- [¿What is Shell?](#what-is-shell)
- [Shell Prompt](#shell-prompt)
- [How to determine Shell](#how-to-determine-shell)
- [Let’s write our first script](#lets-write-our-first-script)
- [Shebang](#shebang)
- [Types of Shell](#types-of-shell)
- [Basic Commands](#basic-commands)
- [Daily use Examples of Shell scripting by System Admins](#daily-use-examples-of-shell-scripting-by-system-admins)
- [Basic GREP command](#basic-grep-command)
- [Shell Scripting Topics](#shell-scripting-topics)
- [Reference](#reference)

## ¿What is CLI and GUI?

CLI is a command line interface. This user interface enables the user to give commands to interact with the device.

GUI is a graphical user interface. This user interface enables users to interact with devices with the help of graphical icons and visual indicators.

## ¿Why would we use CLI over GUI?

- CLI gives better control to the user.
- CLI is a best option for professionals who work on more programming languages.
- It required less memory as compared to GUI.
- The speed of the CLI is faster than GUI.

## ¿What is Shell?

**Shell** is a UNIX term for an interface between a user and an operating system service. Shell provides users with an interface and accepts human-readable commands into the system and executes those commands which can run automatically and give the program’s output in a shell script.

An Operating is made of many components, but its two prime components are

- Kernel
- Shell

![route](https://miro.medium.com/max/1070/0*ktxaBaI7oYQ4HgC6.png)

**Shell Scripting** is an open-source computer program designed to be run by the Unix/Linux shell. Shell Scripting is a program to write a series of commands for the shell to execute. It can combine lengthy and repetitive sequences of commands into a single and simple script that can be stored and executed anytime which, reduces programming efforts.

- /bin/bash and /bin/sh is interactive shell
- /sbin/nologin shell is non-interactive shell

## Shell Prompt

The prompt, **$**, which is called the **command prompt**, is issued by the shell. While the prompt is displayed, you can type a command.

Shell reads your input after you press **Enter**. It determines the command you want executed by looking at the first word of your input. A word is an unbroken set of characters. Spaces and tabs separate words.

Following is a simple example of the **date** command, which displays the current date and time −

```bash
date
```

## How to determine Shell

You can get the name of your shell prompt, with following command :

```bash
echo $SHELL
```

The $ sign stands for a shell variable, echo will return the text whatever you typed in.

## Let’s write our first script

```bash
# !/bin/bash
echo "My First Script!"
```

To run it,

```bash
chmod +x script.sh
```

```bash
./script.sh
```

## Shebang

You might have noticed in above script that it starts with `#!/bin/bash` This is called shebang. It is basically to refer the path to the interpreter. There are many interpreters, some of them are: bash, zsh, csh and ksh, etc.

![](https://miro.medium.com/max/1100/0*ai3K1AxGYG6k8ca2.png)

All the best people in life seem to like LINUX. — Steve Wozniak

To use bash: `#!/bin/bash`  
To use zsh: `#!/bin/zsh`  
To use ksh: `#!/bin/ksh`  
To use csh: `#!/bin/csh`

**Why Shebang?**
`#` is often called sharp and `!` is called Bang, hence the name sharp bang, but generally people say it **shebang** instead of sharp bang.

> **Note** If a script does not contain the shebang, the commands are executed using your shell, so there are chances that the code might run properly, but still, that isn’t the correct way of doing it!

**Comments**  
Comments are started by a `#` sign, anything after pound sign on that line is ignored.

## Types of Shell

There are two main shells in Linux:

1. The **Bourne Shell**: The prompt for this shell is $ and its derivatives are listed below:

   - POSIX shell also is known as sh
   - Korn Shell also knew as sh
   - **B**ourne **A**gain **SH**ell also knew as bash (most popular)

2. **The C shell**: The prompt for this shell is %, and its subcategories are:

   - C shell also is known as csh
   - Tops C shell also is known as tcsh

## Basic Commands

| Name  | Descrption                                                                   |
| ----- | ---------------------------------------------------------------------------- |
| ls    | List the contents of a directory                                             |
| pwd   | Print Working Directory                                                      |
| cd    | Change Directory                                                             |
| cat   | Concatenate and Print the contents of file(s)                                |
| tac   | Concatenate and Print the contents of file(s) in reverese.                   |
| rev   | Reverse the lines of file(s)                                                 |
| man   | Display the Manual Page for a command                                        |
| cp    | Copy file(s) or directory(ies)                                               |
| mv    | Move or Rename file or directory                                             |
| rm    | Remove file(s) or directory(ies)                                             |
| mkdir | Make directory                                                               |
| rmdir | Remove “an empty” directory                                                  |
| date  | Print or Set the system date and time.                                       |
| touch | Change file(s) timestamps. If the file(s) don’t exist, it will be created.   |
| more  | Print file contents one screen at a time.                                    |
| less  | Similar to more , but allows both forward and backward movement in the file. |
| seq   | Print a sequence of numbers between Start and End.                           |
| echo  | Print line(s) of text to the standard output (screen).                       |
| cal   | Display the Calendar (of month or entire year)                               |
| clear | Clear the terminal screen.                                                   |

## Daily use Examples of Shell scripting by System Admins

- Monitoring your Linux system.
- Data backup and creating snapshots.
- Dumping Oracle or MySQL database for backup.
- Creating email based alert systems.
- Find out what processes are eating up your system resources.
- Find out available and free memory.
- Find out all logged in users and what they are doing.
- Find out if all necessary network services are running or not. For example if the web server failed then send an alert to the system administrator via a pager or an email.
- Find out all failed login attempts, if login attempts are continued repeatedly from the same network IP automatically block all those IPs accessing your network/service via firewall.
- User administration as per your own security policies.
- Find out information about local or remote servers.
- Server configuration.

## Basic GREP command

The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern. The pattern that is searched in the file is referred to as the regular expression (grep stands for globally search for regular expression and print out).

```bash
grep [options] pattern [files]
```

**Options Description**  
**-c** : This prints only a count of the lines that match a pattern  
**-h :** Display the matched lines, but do not display the filenames.  
**-i :** Ignores, case for matching  
**-l :** Displays list of a filenames only.  
**-n :** Display the matched lines and their line numbers.  
**-v :** This prints out all the lines that do not matches the pattern  
**-e exp :** Specifies expression with this option. Can use multiple times.  
**-f file :** Takes patterns from file, one per line.  
**-E :** Treats pattern as an extended regular expression (ERE)  
**-w :** Match whole word  
**-o :** Print only the matched parts of a matching line,  
 with each such part on a separate output line.**-A n** **:** Prints searched line and nlines after the result  
**-B n :** Prints searched line and n line before the result.  
**-C n :** Prints searched line and n lines after before the result.

## Shell Scripting Topics

1. [Variables](https://www.shellscript.sh/variables1.html)
2. [Wildcards](https://www.shellscript.sh/wildcards.html)
3. [Escape Characters](https://www.shellscript.sh/escape.html)
4. [Loops](https://www.shellscript.sh/loops.html)
5. [Functions](https://www.shellscript.sh/functions.html)
6. [Test](https://www.shellscript.sh/test.html)
7. [Quck Reference](https://www.shellscript.sh/quickref.html)
8. [Shell Scripting Guide](https://www.shellscript.sh/index.html)

## Reference

- [Shell Scripting Tutorial](https://www.shellscript.sh/index.html)
- [Shell Scripting Medium](https://medium.com/nerd-for-tech/shell-scripting-e95af96aed1b)
- [Bashsxripting for Begginners](https://help.ubuntu.com/community/Beginners/BashScripting)
