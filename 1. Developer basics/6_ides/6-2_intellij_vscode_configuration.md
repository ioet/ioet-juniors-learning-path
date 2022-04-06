# JetBrains IDEs and VSCode Configuration

In this document you will find the most useful tips to configure your JetBrains IDEs and VSCode, also some tips that will make you more productive.

## Authors

- Jean Carlos Alarcón @jcalarcon98
- Javier Sarango @jase156

## Topics

- [JetBrains IDEs and VSCode Configuration](#jetbrains-ides-and-vscode-configuration)
  - [Authors](#authors)
  - [Topics](#topics)
  - [JetBrains IDEs configuration](#jetbrains-ides-configuration)
    - [Customize Colors and Fonts](#customize-colors-and-fonts)
    - [Configure keyboard shortcuts](#configure-keyboard-shortcuts)
    - [Improve menus and toolbars usage](#improve-menus-and-toolbars-usage)
    - [Share IDE Settings](#share-ide-settings)
    - [Install Plugins](#install-plugins)
    - [Create Live Templates](#create-live-templates)
    - [Customize Run/Debug configurations](#customize-rundebug-configurations)

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
