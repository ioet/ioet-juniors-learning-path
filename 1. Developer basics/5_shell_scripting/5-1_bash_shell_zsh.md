# Shell: Bash vs Zsh

## What is Shell?
Shell is a program that takes commands from the keyboard and gives them to the operating system to perform. In the old days, it was the only user interface available on a Unix-like system such as Linux. Nowadays, we have graphical user interfaces (GUIs) in addition to command line interfaces (CLIs) such as the shell.

On most Linux systems a program called bash (which stands for Bourne Again SHell, an enhanced version of the original Unix shell program, sh, written by Steve Bourne) acts as the shell program. Besides bash, there are other shell programs available for other systems. These include: ksh, tcsh and zsh.

Check the difference about Terminal and Shell in the next video:

[![Shell vs Terminal](https://i.ibb.co/2ZVH7g8/image.png)](https://www.youtube.com/watch?v=Yt57-gg9jVg "Shell vs Terminal")

Check the following free course about Shell: [Udacity link](https://www.udacity.com/course/ud595)

<br />

## Bash vs Zsh
There are two widely used shells by the community: Bash and Zsh. The Bash is considered the most widely used shell. At the same time, Z shell or Zsh becomes more and more popular nowadays. So, which terminal you should choose?.

For the most part bash and zsh are almost identical which is a relief. Navigation is the same between the two. The commands you learned for bash will also work in zsh although they may function differently on output. The only thing is Zsh seems to be much more customizable than bash.

### Features comparison
| Zsh                                                                                           | Bash                                                                          |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| It contains a lot of advanced features.                                                       | It does not contain advanced features.                                        |
| Has a more complex configuration file structure.                                              | Configuration files structure is simple.                                      |
| Configuration and customization is provided by Oh My Zsh framework.                           | Configuration and customization is provided by Bash-it.                       |
| Commands history is shared across all shells.                                                 | History sharing is difficult.                                                 |
| Zsh scripts are not so widely used.                                                           | Bash scripts are widely used.                                                 |
| Zsh does not load SHELLOPTS during startup.                                                   | SHELLOPTS are loaded during the start.                                        |
| Environment configuration is more customizable with zshrc, zlogin, zshenv, zlogout, zprofile. | Environment is less customizable and can be implemented with a fewer scripts. |
| Allows using expanded aliases anywhere in the file.                                           | Bash does not support the expanded aliases by default.                        |
| zparseopts makes scripts arguments parsing very easy.                                         | Parsing script arguments with getopts is a bit more challenging.              |
| Terminal calculations can be done using zcalc.                                                | You need to use two external calculators: bc and expr.                        |
| Terminal configuration/autostart scripts are loaded from ~/.zshrc file.                       | Terminal configuration/autostart scripts are loaded from ~/.bashrc file.      |
| bindkey is used for keys binding.                                                             | bind builtin and ~/.inputrc are used for key binding.                         |
| More options to build fancy prompts.                                                          | Less options for fancy prompts.                                               |
| setopt responsible for shell settings.                                                        | shopt configures shell settings.                                              |
| # is not considered a comment unless INTERACTIVE_COMMENTS is set.                             | # represents a comment string.                                                |
| Extended wildcard patterns enabled by default.                                                | Use shopt -s extglob to enable extended wildcard patterns.                    |
| More ways to transform the variable value (parameter expansion).                              | Fewer methods for transforming variables.                                     |
| Has auto completion and spellings correction features embedded.                               | You need to use bash-completion package.                                      |
| More plugins and themes available.                                                            | Fewer plugins and themes available.                                           |
| Zsh is more customizable.                                                                     | Bash is less customizable.                                                    |
| POSIX compatible if emulate sh has been set.                                                  | Follow POSIX standards if --posix command-line option was set.                |
| Auto completion works faster.                                                                 | Auto completion is slower.                                                    |
| Smaller community                                                                             | Wider community                                                               |

<br />

### Internet search volume
Here's a Google Trends [chart](https://trends.google.com/trends/explore?q=ZSH,%2Fm%2F01g7l), which show the search volume comparison for both shells:

<a href="https://ibb.co/jr3F0Ps"><img src="https://i.ibb.co/XCFT0rM/bash-zsh.png" alt="bash-zsh" border="0"></a>