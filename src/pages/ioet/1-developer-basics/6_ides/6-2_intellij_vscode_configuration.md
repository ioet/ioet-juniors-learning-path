---
layout: "../../../../layouts/BlogPost.astro"
title: "JetBrains IDEs and VSCode Configuration"
pubDate: "2022-09-14"
---

In this document you will find the most useful tips to configure your JetBrains IDEs and VSCode, also some tips that will make you more productive.

## Contributors

- [Jean Carlos Alarcón](https://github.com/jcalarcon98)
- [Javier Sarango](https://github.com/jase156)

## Content

- [Contributors](#contributors)
- [Content](#content)
- [JetBrains IDEs configuration](#jetbrains-ides-configuration)
  - [Customize Colors and Fonts](#customize-colors-and-fonts)
  - [Configure keyboard shortcuts](#configure-keyboard-shortcuts)
  - [Improve menus and toolbars usage](#improve-menus-and-toolbars-usage)
  - [Share IDE Settings](#share-ide-settings)
  - [Install Plugins](#install-plugins)
  - [Create Live Templates](#create-live-templates)
  - [Customize Run/Debug configurations](#customize-rundebug-configurations)
- [Visual Studio Code configuration](#visual-studio-code-configuration)
  - [Configuring the editor](#configuring-the-editor)
  - [Side by side editing](#side-by-side-editing)
  - [Editor Groups](#editor-groups)
  - [Grid editor layout](#grid-editor-layout)
  - [Color Themes](#color-themes)
  - [Extension](#extension)
  - [Debugging/Run](#debuggingrun)
  - [Linter](#linter)

## JetBrains IDEs configuration

It is important to clarify that the configuration work in the same way in any of the IDEs that JetBrains offers.

### [Customize Colors and Fonts](https://www.jetbrains.com/help/pycharm/configuring-colors-and-fonts.html)

When you are coding, you work with a lot of text resources: code editor, search results, debugger information, etc. Color and fonts help you better understand it.

### [Configure keyboard shortcuts](https://www.jetbrains.com/help/pycharm/configuring-keyboard-and-mouse-shortcuts.html)

We already learned about a lot of shortcuts that Jetbrains IDEs offers to us. As you might notice these resources could be difficult to memorize. For that reason we can customize all the shortcuts according to our needs.

### [Improve menus and toolbars usage](https://www.jetbrains.com/help/pycharm/customize-actions-menus-and-toolbars.html)

When you work with your IDE, you perform some actions more often than others. Most of the time is better to keep only the things that you use in order to maximize your productivity. In any JetBrains IDEs you can customize the menus and toolbars to only contains the actions that you need, regroup them and also configure their icons.

### [Share IDE Settings](https://www.jetbrains.com/help/idea/sharing-your-ide-settings.html)

It is very common to use these IDEs on different machines and also in different operating systems and you would like to keep the same shortcuts and configuration in your editor regardless of the machine or OS you are using, for that reason is essential to share your IDE settings.

### [Install Plugins](https://www.jetbrains.com/help/pycharm/managing-plugins.html)

If you want to extend the core functionality of any JetBrains IDE, you can install plugins to get additional features, like:

- Extra themes for your IDE.

- Coding assistance support for different languages and frameworks.

- Shortcut hints, file watchers, and so on.

### [Create Live Templates](https://www.jetbrains.com/help/pycharm/creating-and-editing-live-templates.html)

Most of the time, when you are coding, there are a lot of custom code sections that are most often used, for example I use [pdb](https://docs.python.org/3/library/pdb.html) as a python debugger and always when I need to debug some code I need to put the next lines:

``` python
import pdb;
pdb.set_trace()
```

As you can see it is a small piece of code, however, having to repeat it every time I need to debug something, it takes me a few seconds to write it, to avoid this, exists **Live Templates**.

Now when I need to put a debug point, I just have to type `pdb` and automatically the IDE completes the necessary code.

### [Customize Run/Debug configurations](https://www.jetbrains.com/help/pycharm/run-debug-configuration.html)

Each project has its own complexity, et's suppose we have to perform the following steps to set up our project:

1. Export environment variables (`export TOKEN=CuStOm-ToKeN`)

2. Up database container (`docker-compose up`)

3. Fill database tables with shell script (`./fill-database.sh`)

4. Run Project (`python manage.py runserver`)

As you can see, execute these all steps everytime I need to run the application is a lot of work, but we can convert these 4 steps in only one click (or shortcut).

## Visual Studio Code configuration

You can configure Visual Studio Code to your liking through its various settings. Nearly every part of VS Code's editor, user interface, and functional behavior has options you can modify.

### [Configuring the editor](#https://code.visualstudio.com/docs/getstarted/userinterface#_configuring-the-editor)

VS Code gives you many options to configure the editor. From the **View** menu, you can hide or toggle various parts of the user interface, such as the **Side Bar**, **Status Bar**, and **Activity Bar**.

Most editor configurations are kept in settings which can be modified directly. You can set options globally through user settings or per project/folder through workspace settings. Settings values are kept in a `settings.json` [file](#https://code.visualstudio.com/docs/getstarted/settings#_settingsjson).

> **Note for macOS users**: The **Preferences** menu is under Code not File. For example, Code > Preferences > Settings.

- Select **File** > **Preferences** > **Settings** (or press `Ctrl+,`) to edit the user `settings.json` file.
- To edit workspace settings, select the **WORKSPACE SETTINGS** tab to edit the workspace `settings.json` file.

### [Side by side editing](#https://code.visualstudio.com/docs/getstarted/userinterface#_side-by-side-editing)

Visual Studio Code allows open as many editors as you like side by side vertically and horizontally. If you already have one editor open, there are multiple ways of opening another editor to the side of the existing one:

- `Alt` click on a file in the Explorer.
- `Ctrl+\` to split the active editor into two.
- **Open to the Side** (`Ctrl+Enter`) from the Explorer context menu on a file.
- Click the **Split Editor** button in the upper right of an editor.
- Drag and drop a file to any side of the editor region.
- `Ctrl+Enter` (macOS: `Cmd+Enter`) in the Quick Open (`Ctrl+P`) file list.

### [Editor Groups](#https://code.visualstudio.com/docs/getstarted/userinterface#_editor-groups)

When you split an editor (using the **Split Editor** or **Open to the Side** commands), a new editor region is created which can hold a group of items. You can open as many editor regions as you like side by side vertically and horizontally.

### [Grid editor layout](https://code.visualstudio.com/docs/getstarted/userinterface#_grid-editor-layout)

By default, editor groups are laid out in vertical columns (for example when you split an editor to open it to the side). You can easily arrange editor groups in any layout you like, both vertically and horizontally:

There are a predefined set of editor layouts in the new **View** > **Editor Layout** menu. Editors that open to the side will by default open to the right-hand side of the active editor. If you prefer to open editors below the active one, configure the new setting `workbench.editor.openSideBySideDirection: down`.

### [Color Themes](#https://code.visualstudio.com/docs/getstarted/themes)

Color themes let you modify the colors in Visual Studio Code's user interface to suit your preferences and work environment.

### [Extension](#https://code.visualstudio.com/docs/editor/extension-marketplace)

The features that Visual Studio Code includes out-of-the-box are just the start. VS Code extensions let you add languages, debuggers, and tools to your installation to support your development workflow.

You can browse and install extensions from within VS Code. Bring up the Extensions view by clicking on the Extensions icon in the **Activity Bar** on the side of VS Code or the **View: Extensions** command (`Ctrl+Shift+X`). To install an extension, select the **Install** button. Once the installation is complete, the **Install** button will change to the **Manage** gear button.

### [Debugging/Run](#https://code.visualstudio.com/docs/editor/debugging)

To run or debug a simple app in VS Code, select Run and Debug on the Debug start view or press F5 and VS Code will try to run your currently active file.

However, for most debugging scenarios, creating a launch configuration file is beneficial because it allows you to configure and save debugging setup details. VS Code keeps debugging configuration information in a `launch.json` file located in a `.vscode` folder in your workspace (project root folder) or in your [user settings](#https://code.visualstudio.com/docs/editor/debugging#_global-launch-configuration) or [workspace settings](#https://code.visualstudio.com/docs/editor/multi-root-workspaces#_workspace-launch-configurations).

To create a `launch.json` file, click the create a launch.json file link in the Run start view. VS Code will try to automatically detect your debug environment, but if this fails, you will have to choose it manually.

### Linter

To configure the linter according to the programming language, we can use the [Extensions](#https://marketplace.visualstudio.com/VSCode), here we will find lint rules for all languages and when we install them VS code will detect the language and activate the linter.
