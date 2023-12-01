# Introduction

## Why Python?

Python is a highly versatile programming language. It can be used for a number of things which include but are not limited to web development, data analysis, and machine learning. There is a wide range of libraries that can be used to add extra functionality to your code. 

Python also has the benefit of being able to interact with other software such as Touch Designer, Unreal Engine and Unity.

## Installing Miniforge

Miniforge is a distribution of Conda, a package manager and environment management system that simplifies package installation and dependency management. It is helpful because it allows us to manage seperate Python environments for our different projects. Follow the steps below to install Miniforge on your system.

### Windows

1. Go to the [Miniforge GitHub page](https://github.com/conda-forge/miniforge#miniforge3)
2. Download the Windows installer and run the setup file
3. Choose "Run anyway" if a Windows Defender message pops up
3. Choose the default installation options **until** the Advanced Installation Options menu
4. In Advanced Installation Options menu tick the box for "Register Miniforge3 as my default Python 3.10"

![](./pictures/register-minforge.png)

5. Click Install

Once the installation is complete, you should now be able to access a program called "Miniforge prompt." Open the prompt and enter either `conda` or `mamba`. You should see that both will now work on your system.

![](./pictures/miniforge-conda-windows.png)

Entering `python --version` should show that Python 3.10 is now in what is known as your _base environment_. 

![](./pictures/miniforge-python-version-windows.png)

### macOS

In MacOS you can install Miniforge by running a script or by using Homebrew.

#### Script Install

1. Go to the [Miniforge GitHub page](https://github.com/conda-forge/miniforge#miniforge3)
2. Download the appropriate macOS script for your system
3. Open the terminal in the script download path
4. Enter the command `chmod +x Miniforge3-MacOSX-x86_64.sh` or `chmod +x Miniforge3-MacOSX-arm64.sh` depending on which install script you downloaded
5. Execute the script by entering its filename in the terminal and pressing enter
6. Enter yes to accept the license terms when prompted
7. Press enter to confirm the install location when prompted
8. Enter yes to initialise Miniforge3 bu running conda init when prompted

#### Homebrew Install

Open a terminal and enter the following command:

```
brew install miniforge
```
#### Verify macOS Installation

Open a new terminal and type either `conda` or `mamba`. You should see that both will now work on your system.

![](./pictures/miniforge-conda-mac.png)

Entering `python --version` should show that Python 3.10 is now in what is known as your _base environment_. 

![](./pictures/miniforge-python-version-mac.png)

## Installing VSCode
## Many Kinds of Python
## Summary

- Python is a versatile programming language that can be used in various different ways
- To most effectively manage different requirements for different Python projects, we use virtual environments
- Conda and Mamaba enable us to create virtual environments quickly, and also allows us to install libraries
- VSCode is a popular editor for Python development
- Python can be used in an interactive mode, in a notebook, or in a Python file

---
[Next](variables.md) | [List of Contents](README.md)