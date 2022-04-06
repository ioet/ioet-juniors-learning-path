# VIM shortcuts and configuration

In this document you will find the most useful shortcuts for VIM, also some tips that will make you more productive.

[Vim](https://www.vim.org/) is configurable text editor built to make creating any kind of text in efficient way.

## Authors

- Jean Carlos Alarcón @jcalarcon98
- Javier Sarango @jase156

## Topics

- [VIM shortcuts and configuration](#vim-shortcuts-and-configuration)
  - [Authors](#authors)
  - [Topics](#topics)
  - [Shortcuts](#shortcuts)
    - [Global](#global)
    - [Cursor movement](#cursor-movement)
    - [Inserting/appending text](#insertingappending-text)
    - [Editing](#editing)
    - [Exiting](#exiting)

## Shortcuts

Below you will find all the most commonly used shortcuts in Vim.

### Global

| Function                    | Shortcut                         |
| --------------------------- | -------------------------------- |
| Open help for keyword       | `:h[elp] keyword`                |
| Save file as                | `:sav[eas] file`                 |
| Close current pane          | `:clo[se]`                       |
| Open a terminal window      | `:ter[minal]`                    |

### Cursor movement

| Function                             | Shortcut      |
| ------------------------------------ | ------------- |
| Move cursor left                     | `h`           |
| Move cursor down                     | `j`           |
| Move cursor up                       | `k`           |
| Move cursor right                    | `l`           |
| Move cursor down (multi-line text)   | `gj`          |
| Move cursor up (multi-line text)     | `gk`          |
| Move to top of screen                | `H`           |
| Move to middle of screen             | `M`           |
| Move to bottom of screen             | `L`           |
| Jump to the start of the line        | `0`           |
| Jump to the end of the line          | `$`           |
| Go to the first line of the document | `gg`          |
| Go to the last line of the document  | `G`           |
| Go to line 5                         | `5gg` or `5G` |
| Move to local declaration            | `gd`          |
| Move to global declaration           | `gD`          |

> **Tip:** Prefix a cursor movement command with a number to repeat it. For example, 4j moves down 4 lines.

### Inserting/appending text

| Function                                                  | Shortcut      |
| --------------------------------------------------------- | ------------- |
| Insert before the cursor                                  | `i`           |
| Insert at the beginning of the line                       | `I`           |
| Insert (append) after the cursor                          | `a`           |
| Insert (append) at the end of the line                    | `A`           |
| Append (open) a new line below the current line           | `o`           |
| Append (open) a new line above the current line           | `O`           |
| Insert (append) at the end of the word                    | `ea`          |
| Delete the character before the cursor during insert mode | `Ctrl + h`    |
| Delete word before the cursor during insert mode          | `Ctrl + w`    |

### Editing

| Function                                                  | Shortcut      |
| --------------------------------------------------------- | ------------- |
| Replace a single character                                | `r`           |
| Replace more than one character, until ESC is pressed.    | `R`           |
| Change (replace) entire line                              | `cc`          |
| Change (replace) to the end of the line                   | `C`           |
| Undo                                                      | `u`           |
| Restore (undo) last changed line                          | `U`           |
| Redo                                                      | `Ctrl + r`    |

### Exiting

| Function                                                  | Shortcut             |
| --------------------------------------------------------- | -------------------- |
| Write (save) the file, but don't exit                     | `:w`                 |
| Write out the current file using sudo                     | `:w !sudo tee %`     |
| Write (save) and quit                                     | `:wq` or `x` or `ZZ` |
| Quit (fails if there are unsaved changes)                 | `:q`                 |
| Quit and throw away unsaved changes                       | `:q` or `ZQ`         |
| Write (save) and quit on all tabs                         | `:wqa`               |

As you can see, there are a lot of shortcuts for Vim, however. there are many more, here you can find an excellent [spreadsheet](https://vim.rtorr.com/) with a lot of extra shortcuts that will alow you to be much more productive with Vim.

