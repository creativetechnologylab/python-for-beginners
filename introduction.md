# Introduction

## Why Python?

Python stands out as a remarkably versatile programming language, finding utility across diverse domains such as web development, data analysis, and machine learning. Its strength lies in its extensive library support, offering a broad spectrum of additional functionalities for your code.

Moreover, Python excels in interoperability, allowing interaction with other software tools like Touch Designer, Unreal Engine, and Unity.

## Installing Miniforge

Miniforge, a distribution of Conda, serves as a comprehensive package manager and environment management system, simplifying the complexities of package installation and dependency management. Its utility lies in the ability to manage separate Python environments for different projects. Follow the steps below to install Miniforge on your system.

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
8. Initialize Miniforge3 by running `conda init` when prompted.

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

## Installing VSCode
## Many Kinds of Python
## Summary

- Python is a versatile programming language.
- To effectively manage diverse Python project requirements, we employ virtual environments.
- Conda and Mamba facilitate quick creation of virtual environments and library installations.
- VSCode stands out as a popular editor for Python development.
- Python can be used in an interactive mode, in notebooks, or in standard Python files.

---
[Next](variables.md) | [List of Contents](README.md)