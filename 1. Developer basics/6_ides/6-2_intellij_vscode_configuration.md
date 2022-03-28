# JetBrains IDEs and VSCode Configuration

## JetBrains IDEs configuration

It is important to clarify that the configuration work in the same way in any of the IDEs that JetBrains offers.

### Customize Colors and Fonts

When you are coding, you work with a lot of text resources: code editor, search results, debugger information, etc. Color and fonts help you better understand it. Here is a [excellent guide](https://www.jetbrains.com/help/pycharm/configuring-colors-and-fonts.html) to customize colors and fonts.

### Configure keyboard shortcuts

In the previous lecture, we learned about a lot of shortcuts that Jetbrains IDEs offers to us. As you might notice these resources could be difficult to memorize. For that reason we can customize all the shortcuts. Here you can find an [excellent resource](https://www.jetbrains.com/help/pycharm/configuring-keyboard-and-mouse-shortcuts.html) on how to customize these shortcuts.

### Improve menus and toolbars usage

When you work with your IDE, you perform some actions more often than others. Most of the time is better to keep only the things that you use in order to maximize your productivity. In any JetBrains IDEs you can customize the menus and toolbars to only contains the actions that you need, regroup them and also configure their icons. [Here](https://www.jetbrains.com/help/pycharm/customize-actions-menus-and-toolbars.html) you can find a section where it is explained how to achieve these.

### Share IDE Settings

It is very common to use these IDEs on different machines and also in different operating systems and you would like to keep the same shortcuts and configuration in your editor regardless of the machine or OS you are using, for that reason is essential to share your IDE settings. In this [guide](https://www.jetbrains.com/help/idea/sharing-your-ide-settings.html), you can find different ways to share your IDE settings, choose the one you like.

### Install Plugins

If you want to extend the core functionality of any JetBrains IDE, you can install plugins to get additional features, like:

- Extra themes for your IDE.

- Coding assistance support for different languages and frameworks.

- Shortcut hints, file watchers, and so on.

[Here](https://www.jetbrains.com/help/pycharm/managing-plugins.html) you can find how to install external plugins in your IDE.

### Create Live Templates

Most of the time, when you are coding, there are a lot of custom code sections that are most often used, for example I use [pdb](https://docs.python.org/3/library/pdb.html) as a python debugger and always when I need to debug some code I need to put the next lines:

``` python
import pdb;
pdb.set_trace()
```

As you can see it is a small piece of code, however, having to repeat it every time I need to debug something, it takes me a few seconds to write it, to avoid this, exists **Live Templates**.

Now when I need to put a debug point, I just have to type `pdb` and automatically the IDE completes the necessary code. Here you can find a [tutorial](https://www.jetbrains.com/help/pycharm/creating-and-editing-live-templates.html) to create your own live templates.

### Customize Run/Debug configurations

Each project has its own complexity, et's suppose we have to perform the following steps to set up our project:

1. Export environment variables (`export TOKEN=CuStOm-ToKeN`)

2. Up database container (`docker-compose up`)

3. Fill database tables with shell script (`./fill-database.sh`)

4. Run Project (`python manage.py runserver`)

As you can see, execute these all steps everytime I need to run the application is a lot of work, but we can convert these 4 steps in only one click (or shortcut).

With any of JetBrains IDEs we can configure these 4 steps in a single **Run/Debug configuration**, [here](https://www.jetbrains.com/help/pycharm/run-debug-configuration.html) you can follow these steps to achieve this.
