# Introduction

## Why Python?

Python is a highly versatile programming language, making it suitable for diverse domains such as web development, data analysis, and machine learning. One very important strength of Python is its extensive library support, which allow you to add a broad spectrum of additional functionalities for your code.

Moreover, Python can be used to interface with other software tools like Touch Designer, Unreal Engine, and Unity.

<!-- todo: why install miniforge, v envs, etc -->

## Installing Miniforge

Miniforge, a distribution of Conda, serves as a comprehensive package manager and environment management system, simplifying package installation and dependency management. Its utility lies in the ability to manage separate Python environments for different projects. This in turn prevents issues from arising if different projects require different versions of Python or different versions of the same library. Another advantage of using environments is that they can easily be deleted once a project has been completed, which allows us to keep our core Python installation "clean" from add-ons that are no longer needed. Follow the steps below to install Miniforge on your system.

### Windows

1. Navigate to the [Miniforge GitHub page](https://github.com/conda-forge/miniforge#miniforge3).
2. Download the Windows installer and run the setup file.
3. Choose "Run anyway" if a Windows Defender message appears.
4. Opt for the default installation options **until** the Advanced Installation Options menu.
5. In the Advanced Installation Options menu, select "Register Miniforge3 as my default Python 3.10."

    ![Register Miniforge](./pictures/register-minforge.png)

6. Click Install.

Upon completion of the installation, you should be able to access a program called "Miniforge prompt." Open the prompt and enter either `conda` or `mamba` to confirm their functionality on your system.

![Miniforge Conda Windows](./pictures/miniforge-conda-windows.png)

Entering `python --version` should indicate that Python 3.10 is now part of your _base environment_. You will learn more about this later.

![Miniforge Python Version Windows](./pictures/miniforge-python-version-windows.png)

### macOS

For macOS, you can install Miniforge using a script or through Homebrew.

#### Script Install

1. Visit the [Miniforge GitHub page](https://github.com/conda-forge/miniforge#miniforge3).
2. Download the appropriate macOS script for your system.
3. Open the terminal in the script download path.
4. Execute the command `chmod +x Miniforge3-MacOSX-x86_64.sh` or `chmod +x Miniforge3-MacOSX-arm64.sh` based on the install script downloaded.
5. Run the script by entering `./Miniforge3-MacOSX-x86_64.sh` or `./Miniforge3-MacOSX-arm64.sh` in the terminal depending on your install script and press enter.
6. Accept the license terms when prompted by entering yes.
7. Confirm the install location by pressing enter when prompted.
8. Enter yes when prompted to initialise Miniforge3 by running conda init.

#### Homebrew Install

In a terminal, enter the following command:

```bash
brew install miniforge
```
#### Verify macOS Installation

Verify the macOS installation by opening a new terminal and typing either `conda` or `mamba`.

![Miniforge Conda macOS](./pictures/miniforge-conda-mac.png)

Entering `python --version` should indicate that Python 3.10 is now part of your _base environment_. You will learn more about this later.

![Miniforge Python Version macOS](./pictures/miniforge-python-version-mac.png)

## Installing VS Code

This guide introduces Python programming through the use of Visual Studio Code (VS Code), a versatile Integrated Development Environment (IDE) developed by Microsoft. IDEs offer a number of useful features for development, such as debugging, testing, Version Control software integration, and auto-completion. In time you'll find such tools will greatly enhance your productivity and will enable you to spot problems earlier. A stitch in time saves nine.

To install VS Code, download the appropriate setup file for your system from [here](https://code.visualstudio.com/download) and go through the setup steps. Alternatively, if you are on a UAL machine, you can use Self-Service if VS Code is not already installed.

## Making VS Code Recognise Conda or Mamba

With VS Code installed, we will now need to make it recognise our Conda/Mamba location. To do this, you must first make sure that VS Code has the Python Extension installed. This may be downloaded by following this [link](https://marketplace.visualstudio.com/items?itemName=ms-python.python).

Now go into your Settings in VS Code by clicking on the cog icon in the bottom-left and then clicking on Settings.

![Miniforge Python Version macOS](./pictures/vscode-settings-1.png)

Type "Conda" in the search to bring up the option for the Conda path.

![Miniforge Python Version macOS](./pictures/vscode-settings-2.png)

Now you need to give it the path of either your Conda or Mamba installation. Both are fine. The steps to do this will vary depending on your system.

### Windows

![Miniforge Python Version macOS](./pictures/where-conda-windows.png)

Open the Miniforge Prompt and type `where conda` or `where mamba`. Copy and paste the first path into the Conda Path field in the VS Code settings. Close the Settings tab.

### MacOS

![Miniforge Python Version macOS](./pictures/whereis-conda-mac.png)

In a terminal type `whereis conda` or `whereis mamba`. Copy and paste the output into the Conda Path field in the VS Code settings. Close the Settings tab.

## Choosing a Python Interpreter

Now that VS Code can see your Conda/Mamba installation, we can use its `base` environment as our interpreter for Python projects.

To do this we press Ctrl + Shift + P (Windows) or Command + Shift + P (Mac) to bring up VS Code's Command Palette.

![](./pictures/command-palette.png)

Type in "Select Interpreter" and you should see the option of choosing a Python interpreter.

![](./pictures/python-interpreter.png)

Clicking this will lead to a drop-down option of possible Python interpreters for our Python files. Select the base Conda/Mamba interpreter. This one will say "Conda" on the right.

![](./pictures/choose-conda-base-interpreter.png)

Now any Python file run within VS Code will make use of the base Conda/Mamba environment by default. We will want to change this later on, but for now this works.

And here are the full steps in a gif.

![](./pictures/select-interpreter.gif)

## Basic Conda / Mamba Usage

When creating a new Python project, it is a good idea to create a separate environment for it. An environment is like a specialised Python installation that has all the libraries needed for a particular project. As you work with Python more, you will find that different projects require different libraries. Creating separate Python environments helps keep things tidy.  

### Creating an Environment

To create an environment, we give the following command:  

Conda:
```
conda create -n <env-name>
```
Mamba:
```
mamba create -n <env-name>
```

By default, this will create an environment with the same Python version as your base environment.

Creating a new environment with a _specific_ version of Python can be done with the following command:

Conda:
```
conda create -n <env-name> python=X.X
```
Mamba:
```
mamba create -n <env-name> python=X.X
```

### Activating / Deactivating Environments

To activate an environment we then use the following command:  

Conda:
```
conda activate <env-name>
```
Mamba:
```
mamba activate <env-name>
```
When an environment has been activated, using the `python` command will cause that particular environment's version of `python` to be used rather than that of the base environment.

Using the `deactivate` command then allows you to return to the base environment:  

Conda:
```
conda deactivate
```
Mamba:
```
mamba deactivate
```

### Installing Libraries

In many cases, a library can be installed through Mamba or Conda. This can be achieved with the following command:

Conda:
```
conda install <library-name>
```
Mamba:
```
mamba install <library-name>
```
Alternatively, a library can also be installed with `pip`. This will also install the library to the environment.

```
pip install <library-name>
```

## Many Kinds of Python

### Terminal

Python can be run in the terminal. This can be useful if you want to do something simple, like checking if a library you've installed is working.

![](./pictures/python-in-terminal.gif)

### Script

We can also use Python scripts. These are files that end in the `.py` extension. Below is an example of a basic Python script being executed. 

![](./pictures/python-script.gif)

### Notebooks

Notebooks are another way of using Python. The notebook for the Introduction to Python workshop can be found [here](https://bit.ly/3F5b88F).

## Summary

- Python is a versatile programming language.
- To effectively manage diverse Python project requirements, we employ virtual environments.
- Conda and Mamba facilitate quick creation of virtual environments and library installations.
- IDEs provide comprehensive tools and features to streamline and facilitate the entire software development process, including code writing, debugging, and project management.
- Python can be used in the terminal, in Python script files, or in notebooks.

---
[List of Contents](README.md) | [Next](getting-started.md)