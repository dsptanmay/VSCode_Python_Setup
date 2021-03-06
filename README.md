# VSCode_Python_Setup

This is a simple guide for setting up VSCode for Python.

I have seen many guides on this same topic but I found many of them unsatisfying.

So, I decided to make my own guide!

#### NOTE: This guide is for Windows based machines.[ Although, most of the steps should be the same for Mac/Linux Machines.]

#### This guide also assumes that you have Python installed on your system already.

Before we get started, here are are some common actions that I will be referring to:

- Opening the command palette:
    - It is a place where we can find all the actions of VSCode easily.
    - To open it, use the shortcut Ctrl+Shift+P

- Opening Settings.json/ adding lines to it.
    - to open Settings.json, hit Ctrl+Shift+P and search for Settings JSON and select the option that says "Preferences: Open Settings(JSON)"

- Opening Settings UI:
    - to open Settings UI, click on the gear icon on the activity bar.(Alternatively, you can search for Settings UI from the Command Palette)

### *Step 1: Installing VSCode:*

This step is pretty self-explanatory. To download VSCode, go to https://code.visualstudio.com/

Download the file as per your device and run it to set it up.

After the installation is complete, you should be greeted with a screen like this:

![Image 1](demo/img_1.png)

----
### *Step 2: Setting Up Python for VSCode:*

First things first, go to the VSCode Extensions Panel (Ctrl+Shift+X on Windows)

![Image 2](demo/img_2.png)


and search for Python.

![Image 3](demo/img_3.png)


Now, click on the Python Extension by Microsoft (It should be the first one)

Click on install and wait for the installation to finish.

![Image 4](demo/img_4.png)

Once the installation is finished, you should see a Python Version on the Status Bar:

![Image 5](demo/img_4_b.png)


Now we have the capability to edit Python Code on VSCode properly!

Some of the features the Python Extension provides are:
- Code Completion
- Code formatting
- Code Linting
- Tests
- Refactoring & More!
----
### *Step 3: Making our workflow better:*

Now that we have installed the Python extension, we can run move onto the next part: 
**Installing and using a Language Server**

----

**What is a Python Language Server?**

A language server, to put it simply is a piece of software that makes our code writing experience better.

It contains some custom features like code analysis, finding references and infering types.

A Python Language Server is a language server is specific to Python and contains Python specific features.

back to the installation...

----

The most up-to-date Python Language Server as of the making of this guide is  ```Pylance```

To install Pylance, simply search for Pylance in the VSCode MarketPlace (***Extensions*** Panel)

![Image 5](demo/img_5.png)

The publisher should be **Microsoft**.


Once it is installed, a window should popup asking you to make Pylance the default Language Server.

![Image 6](demo/img_6.png)

Click on **Yes, and Reload**. 

Once the window has reloaded, Pylance should automatically start analyzing your open Python Files.

Common Error: If you do not see the popup, you can follow the following steps:

- Open Settings(JSON) from the Command Palette
- Add the following line to your settings.json file:
    
```"python.languageServer":"Pylance"```
- If you see an error message saying "Value is not accepted", don't worry! Pylance is not officially in the settings documentation due to which it is shown as an error. **It will work nonetheless**

----

### *Step 4: Installing linters and formatters:*

A python linter is a package which checks our code for errors and helps us to make better code

A python formatter is a package which formats our code according to a particular convention (Usually PEP)

The linter that I personally use is : ```Pylint```.

The formatter that I use is: ```Black```.

To use Pylint as the default linter and black as the default formatter, we have to change a few settings.

Steps to enable Pylint:
- Open the Command Palette (Ctrl+Shift+P)
- Search for Python Linter
- Choose the option that says "Python: Select Linter"

- Choose pylint as your linter.
![Image 8 C](demo/img_8_c.png)

- You will get a popup asking you to install pylint if you haven't already.
![Image 8 A](demo/img_8_a.png)

Steps to enable black:
- Open Settings(UI) from the Command Palette.
![Image 7 A](demo/img_7_a.png)

- Search for Python Formatting Provider 
![Image 7 B](demo/img_7_b.png)

- Change the provider from autopep8 to **black**.

- You will get a popup asking you to install black if it isn't already.
![Image 8 B](demo/img_8_b.png)

Now we have to ensure that we format and lint our file everytime we save our file.

To do so, add the following lines to your setting.json file:

```"python.linting.lintOnSave": true,```

```"editor.formatOnSave": true```

### *Step 5: Making VSCode less cluttered.*

If you look at your VSCode Setup right now, you might be feeling that is a bit cluttered and not a very pleasant editor to look at.

I'll be showing you how to fix that.

----
**First part :** Installing a custom font.

The font that I recommend to others the most is JetBrains Mono. (Although you can use other fonts with font ligatures).

Download JetBrains Mono from this link: https://download.jetbrains.com/fonts/JetBrainsMono-2.001.zip

Extract the file to your desired location. Once extracted, open the folder and go the ***/ttf*** folder.
![Font Img](demo/img_9_a.png)

Click on JetBrains Mono Regular and install it.

![Reg](demo/img_9_b.png)

Once that is done, we need to enable it in VSCode. To do so,

add the following lines to your settings JSON file:

```"editor.fontFamily":"JetBrains Mono",```

```"editor.fontLigatures":true```

(Font ligatures are a way of combining specific characters to make our code easier to read. To learn more about it, visit this [Link](https://www.hanselman.com/blog/MonospacedProgrammingFontsWithLigatures.aspx))

----
**Second Part :** Making the readability better

In our Current Setup, we have JetBrains Mono as our font but if you would notice, it doesn't look very easy to read.

To fix this, we need to change a couple of settings in VSCode.

Open Settings UI, and search for "Line Height"

You should find two options like this:

![Line Height](demo/img_10_a.png)

**Change** the "Editor:Line Height" to ***40*** 

**Change** the "Editor: Suggest Line Height" to ***40*** as well.

You should notice immediately that the file you are working on looks much cleaner and easier to understand at a glance.

While we are here, we will also be changing the font size from the default 14 to 16 simply for better viewing. (You are free to change it to whichever size you prefer)

To change the font size, we once again go into Settings UI and this time, search for "Font Size"

Change the Font Size from 14 to 16.

![Font size](demo/img_10_b.png)

----
**Third Part :** Choosing a good theme

A good theme is essential to any developer's workfow. Working on anything becomes much more fun if you are inclined to do so.

The theme I am currently using is called ***"One Dark Darker"*** (By Joel Crosby). It is available on the Extensions Marketplace and is a port of the famous One Dark Theme.

----
![One Dark Darker](demo/img_10_c.png)

----

To use it simply search for it in the Extensions tab and click on install.

(You can install any other theme to your liking.)

**Fourth Part :** Decluttering the window

Although VSCode has many useful sections within its window, these different sections take up a lot of space and make the workspace feel cluttered overall.

*Section 1 :* Removing the Activity Bar

The Activity Bar is 