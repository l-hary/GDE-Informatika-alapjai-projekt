---
layout: default
title: Python Setup
---
# Python Setup

## Introduction

### Language choice

Even though this document is meant to be used primarily by Hungarian GDE students, as the lingua franca of the IT world is English, it'll be written in English. If you have any questions about the terminology used and cannot find the answer by googling, [reach out](mailto:ga790t@neptun.gde.hu?subject=Question%20about%20Python%20Setup) to me.

### Purpose
The purpose of this document is to assist the reader with setting up a local development environment for Python in Windows. This document does not replace any course materials, nor is it endorsed by the University. Everything included here is based on the author's own knowledge and experience. It is not peer reviewed and might contain errors.
{: .justified}

## Installing Python

Up until now you've probably installed programs by searching for the installer in your preferred search engine (most likely Google), downloading and then running the installer. While this is one solution, one common traits of programmers is that we like to automate and simplify things. You can easily simplify software installations and updates by using a package manager like `winget`. 
{: .justified}

Installation instructions assume that you are using Windows and have administrator rights. 

### Using winget to install Python

1. Open Command Prompt or PowerShell.
2. Search for Python3 to see all available versions:
```sh
winget search python3
```
3. Install Python:
```sh
winget install Python.Python.3.11
```
4. If/when prompted, add Python to PATH

### Adding Python to PATH
Adding Python to the PATH environment variable allows you to run Python and its associated scripts from any command prompt or terminal window using the `python` command without needing to specify the full path to the Python executable.
{: .justified}

### Writing Python code

By invoking the `python` command in the terminal you are now able to write and execute Python code. This is a very basic way to code though, lacking the quality of life features offered by code editors. 

Nonetheless, write 
```python
print('hello world')
```
and execute it by pressing `Enter`. Congratulations, you've created your first program.
{: .justified}

## Installing a Code Editor
Using a code editor, such as Visual Studio Code (VS Code), offers several advantages over writing and executing code directly in the terminal:
{: .justified}

- **Syntax Highlighting**: Colors different parts of your code to make it easier to read and understand.
- **Code Completion**: Suggests possible completions for partially typed words, speeding up coding and reducing typos.
- **Debugging Tools**: Allows you to set breakpoints, inspect variables, and step through code to find and fix bugs.
- **Integrated Terminal**: Run commands without leaving the editor, streamlining your workflow.
- **Extensions and Plugins**: Add functionality such as linters, formatters, and language support to customize the editor to your needs.

By using a code editor, you can significantly improve your productivity and the quality of your code. A common choice is Microsoft Visual Studio Code, commonly referred to as VS Code. Alternatively, you can use the [JetBrains IDEs](https://www.jetbrains.com/community/education/#students) (PyCharm in this case) for free while you are a student. I will focus on VS Code. 

You can use `winget` to install it by executing
```sh
winget install Microsoft.VisualStudioCode
``` 
in the terminal.
{: .justified}

### Setting up VS Code
Most of VS Code's functionality comes from the **Extensions** you've installed. Currently you don't have any. If the *"Get Started with VS Code"* page is still open you can click on *"Rich support for all your languages"*, browse, and install the Python extension. If you've closed the welcome page, click on the *Extensions* button on the sidebar or press `Ctrl+Shift+X`. Installing the main Python extension should install the following:
{: .justified}

- Pylance
- Python
- Python Debugger

I recommend also installing the following extensions:
- [indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow) Python code is structured by using whitespace, this extension helps differentiating between the various indentation levels. 
- [Python Indent](https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent) helps with proper indentation for new lines. 
- [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter) automatically enforces strict styling standards, based on [PEP8](https://peps.python.org/pep-0008/). Requires setup, follow the instructions. Command Palette can be invoked with `Ctrl+Shift+P`

## Summary
You have learned how to install Python and Visual Studio Code (VS Code) using a package manager. You should have a fully functional Python development environment, equipped with tools to enhance your coding experience and maintain code quality.
{: .justified}

You can easily update programs installed through `winget` by using 
```sh
winget update
``` 
to get a list of outdated programs and use 
```sh
winget upgrade --all
```
to update all of them with a single command. 

