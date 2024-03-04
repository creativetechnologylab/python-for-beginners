# Getting Started

## Creating a Python File

We can make a simple Python program to do some maths for us. Start by opening a folder in VS Code.

![](./pictures/vscode-open-folder.png)

Now, using either Explorer (Windows) or Finder (Mac), create a folder named "python-exercises." Make sure the folder is in a location that is easy to remember. Now open the folder and click "Select Folder".

![](./pictures/create-python-folder.gif)

Now we can see that this folder has been opened with VS Code. Click on the "New File" icon to create a new file within the folder.

![](./pictures/create-file-vscode.png)

Name this file "calculator.py". By giving it the `.py` extention, VS Code knows to treat it as a Python file. This will cause the new file to then open in the editor area.

![](./pictures/make-calculator-file.gif)

## `print()` and Using Python as a Calculator

Now enter the code `2 + 2` in your `calculator.py` file and save it. Ctrl / Command + S is a useful shortcut for saving. Your window should now look like this:

![](./pictures/calculator-code.png)

Now we can run our code. We can do this by pressing the Run / Play button in the upper-right corner of the editor region. This will lead to a terminal pane being opened.

![](./pictures/running-calculator-code.gif)

The information in the terminal is telling us is that the base Conda / Mamba Python was used to run our file. However, we don't see anything else because this particular file did not generate any output. If we want to see the _result_ of `2 + 2`, we need to use Python's `print()` command.

Now, instead have the code run `print(2 + 2)` and then save your file and run it again.

![](./pictures/calculator-output.png)

> :information_source: As you were typing out the `print()` command, you may have noticed a box appear with some information about `print()`. This is a feature common to several IDEs called **parameter hints**. These can be helpful in making sure a command is used in the correct way.

## Summary

Todo.

---
[Prev](introduction.md) | [List of Contents](README.md) | [Next](variables.md)