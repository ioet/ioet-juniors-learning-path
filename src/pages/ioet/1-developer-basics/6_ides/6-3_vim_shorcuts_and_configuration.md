---
layout: "../../../../layouts/BlogPost.astro"
title: "VIM shortcuts and configuration"
pubDate: "2022-09-14"
---

In this document you will find the most useful shortcuts for VIM, also some tips that will make you more productive.

[Vim](https://www.vim.org/) is configurable text editor built to make creating any kind of text in efficient way.

## Contributors

- [Jean Carlos Alarcón](https://github.com/jcalarcon98)
- [Javier Sarango](https://github.com/jcalarcon98)

## Content

- [Contributors](#contributors)
- [Content](#content)
- [Shortcuts](#shortcuts)
  - [Global](#global)
  - [Cursor movement](#cursor-movement)
  - [Inserting/appending text](#insertingappending-text)
  - [Editing](#editing)
  - [Exiting](#exiting)
- [Configuration](#configuration)
  - [Basic Settings](#basic-settings)
  - [Fold Long Files in Vim](#fold-long-files-in-vim)
  - [Add Plugins to Vim](#add-plugins-to-vim)

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

## Configuration

You can configure Vim with all your favorite option settings and mappings writing  them to what is called the vimrc file and  Vim executes the commands in this file when starts. You can visit the official [documentation](https://vimdoc.sourceforge.net/htmldoc/usr_05.htm) for further reference.

If you already have a vimrc file (e.g., when your sysadmin has one setup for you), you can edit it this way:

````vim
  :edit $MYVIMRC
````

If you don't have a vimrc file yet, you can create a vimrc file in these recommended locations for your personal initializations:

| System                                                  | Location             |
| --------------------------------------------------------- | -------------------- |
| Unix | $HOME/.vimrc |
| OS/2 |  $HOME/.vimrc or $VIM/.vimrc (or _vimrc) |
| MS-DOS and Win32 | $HOME/_vimrc or $VIM/_vimrc |
| Amiga |  s:.vimrc or $VIM/.vimrc |

Also, the ":version" command mentions the name of the
"user vimrc file" Vim looks for.

You can customize Vim by putting suitable commands in your vimrc. Here is a very simple example:

````vim
    " Always wrap long lines:
    set wrap
````

Lines that begin with `"` are comments and are not read by vim.

### Basic Settings

Syntax highlighting and show line numbers is very useful. The next lines enable syntax highlighting and display line numbers to make your code easier to read.

````vim
  " Turn syntax highlighting on.
  syntax on

  " Add numbers to each line on the left-hand side.
  set number

  " Highlight cursor line underneath the cursor horizontally.
  set cursorline

  " Highlight cursor line underneath the cursor vertically.
  set cursorcolumn
````

Folowing we have some basic settings that will improve your editing experience:

````vim
  " Disable compatibility with vi which can cause unexpected issues.
  set nocompatible

  " Enable type file detection. Vim will be able to try to detect the type of file in use.
  filetype on

  " Enable plugins and load plugin for the detected file type.
  filetype plugin on

  " Load an indent file for the detected file type.
  filetype indent on

  " Set shift width to 4 spaces.
  set shiftwidth=4

  " Set tab width to 4 columns.
  set tabstop=4

  " Use space characters instead of tabs.
  set expandtab

  " Do not save backup files.
  set nobackup

  " Do not let cursor scroll below or above N number of lines when scrolling.
  set scrolloff=10

  " Do not wrap lines. Allow long lines to extend as far as the line goes.
  set nowrap

  " While searching though a file incrementally highlight matching characters as you type.
  set incsearch

  " Ignore capital letters during search.
  set ignorecase

  " Override the ignorecase option if searching for capital letters.
  " This will allow you to search specifically for capital letters.
  set smartcase

  " Show partial command you type in the last line of the screen.
  set showcmd

  " Show the mode you are on the last line.
  set showmode

  " Show matching words during a search.
  set showmatch

  " Use highlighting when doing a search.
  set hlsearch

  " Set the commands to save in history default number is 20.
  set history=1000
````

### Fold Long Files in Vim

The .vimrc file can get long so organizing it into sections is a smart idea. Vim will allow you to fold long files to hide sections of text.

Add the following lines to the bottom of your .vimrc to organize the file into sections.

````vim
  " This will enable code folding.
  " Use the marker method of folding.
  augroup filetype_vim
      autocmd!
      autocmd FileType vim setlocal foldmethod=marker
  augroup END
````

Now, once you move your cursor on a fold you can press:

- `zo` to open a single fold under the cursor.
- `zc` to close the fold under the cursor.
- `zR` to open all folds.
- `zM` to close all folds.

### Add Plugins to Vim

Vim's functionality can be extended by adding plugins. A plugin is nothing more than a Vim script file that is loaded automatically when Vim starts.  You can add a plugin very easily by dropping it in your plugin directory.

There are two types of plugins:

`Global plugin`: Used for all kinds of files, You need copy the plugin file to your plugin directory:

  | System                                                         | Plugin directory             |
| --------------------------------------------------------- | -------------------- |
| Unix | ~/.vim/plugin/ |
| PC and OS/2 | $HOME/vimfiles/plugin or $VIM/vimfiles/plugin |
| Amiga | s:vimfiles/plugin |
| Macintosh | $VIM:vimfiles:plugin |
| Mac OS X | ~/.vim/plugin/ |
| RISC-OS | Choices:vimfiles.plugin |

`Filetype plugin`: Only used for a specific type of file. If you want to use the plugins for filetype you must activate this option putting `:filetype plugin on`  in the .vimrc file.

You can add a filetype plugin by dropping it in the right directory. The name of this directory is in the same directory mentioned above for global plugins, but the last part is "ftplugin".

