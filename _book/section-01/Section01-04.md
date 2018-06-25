# 4. Installing Python and Anaconda (Mac, Linux & Windows)

## DOWNLOADING AND INSTALLING THE REQUIRED PYTHON PACKAGES

### Downloading Python and Anaconda
* Just google for Anaconda Python and go to the website
* You can also directly go to [Anaconda Website](https://www.anaconda.com/download/)
* Select whichever OS you are on for the installer
* So download the Python version and you can get the Cheatsheet if you want
* Ensure the Python version that you are downloading is 3.6 or above

### Python & Anaconda Introduction
* Python is a programming language that we can install onto machine and then on top of that we can install different integrate developement environment (IDEs) and you can add packages onto it.
* You can do lots of different modifications
* So there is this pre-packed solution called Anaconda which installs not only python but installs a couple of IDEs onto your computer.
* Anaconda also installs the most common packages that you might be using like Numpy, Pandas and some others.
* Once it downloaded, just run it and install it your computer.

### Opening and running Anaconda
* Normally, Anaconda can update automatically from the Anaconda Navigator, but Anaconda Navigator may fail to update after restart
* So if you want to update Anaconda manually from your cmd for Windows, input the follow line in your cmd and run in Administrator mode
```
	conda update anaconda-navigator
```

* Open up Anaconda navigator from your start menu
* A couple of things are available in Anaconda, like Jupyter notebook, Qtconsole, Spyder IDE, Glueviz, Jupyterlab, Orange3, Rstudio and Vscode.
* What we are actually interested in, is the Spyder IDE which is our IDE of choice.
* You can also update any package or program from Anaconda navigator inside Environments, and Updateable.
* So let's go ahead and launch Spyder IDE and have a look inside.
* The mac and Windows layout of Spyder IDE may differ so do not be surprised.

### Running and customizing Spyder IDE
* To bring up your panes, go to view and select panes
* You select editor, and you don't need console
* Instead pick Ipython Console, Variable Explorer and also Object inspector.
* If you need other panes, you can always just add them through view, panes
* If you want to increase the font size for Editor and Ipython console, go to Tools, and preferences.
* On the left, find General, and under Appearance, you can increase the font and change the font style. You can maybe increase the font size to 14 or something, depending on your preferences.
* If you want to change the color scheme or anything. Go to Tools, Preferences and pick your desired scheme under Syntax Coloring.
* You can also create a custom color according to your preference under Syntax Coloring, and edit Selected.
* To run your first command on Python, in Spyder IDE
```
	print("Hello World!")
```

* You can press current Cell or current file
* The command is Ctrl-Enter on the highlighted code to run it.
* You should see the output printed on the Ipython console on the right.