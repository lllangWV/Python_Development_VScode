
# Project in VS Code

We will be going over a demonstration of a Python Project in VScode. To start, lets create a new folder and open it in VS Code

- **Step 1:** Open VS Code.
- **Step 2:** Go to `File` > `Add Folder to Workspace...` and create a new folder named `vscode_demo`.
- **Step 3:** Open the new folder in VS Code to start your project.

## 1.Installing Python Extensions

To effectively interface Python with Visual Studio Code (VS Code), installing certain extensions is essential. These extensions enhance the development experience by providing advanced coding support, debugging capabilities, code formatting, and more. Below is a list of recommended extensions for Python development in VS Code:

- **Python**: The main extension for Python development in VS Code, offering comprehensive support for Python, including IntelliSense (powered by Pylance for enhanced coding assistance), linting, debugging, code navigation, formatting, refactoring, and more. This extension supports all actively maintained versions of Python (>=3.7) and enhances your coding experience whether you're working on simple scripts or complex projects. It also includes support for Jupyter Notebooks, test exploration, and environment management, ensuring a versatile development environment.

- **Pylance**: An optional yet highly recommended extension that works alongside the Python extension to provide fast, feature-rich language support. Utilizing Microsoft's Pyright, Pylance supercharges IntelliSense with advanced type information, helping you write more accurate code quickly. It also offers syntax highlighting, code navigation, and type checking, making it a valuable tool for Python developers seeking an improved coding experience.

- **Python Debugger**: Integrated into the Python extension, this tool allows for easy debugging of Python scripts, web apps, remote processes, and multi-threaded programs directly within VS Code. It supports step-through debugging, breakpoints, variable inspection, and more, making it easier to identify and fix issues in your code.

- **autopep8**: A formatting extension that automatically adjusts your Python code to conform to the PEP 8 style guide. With autopep8, you can ensure your code is not only functional but also clean and consistent with Python's coding standards. This extension can be invoked to format a file or an entire project, helping to maintain a professional codebase.

Each of these extensions plays a vital role in streamlining the Python development process in VS Code, from writing and debugging code to ensuring it adheres to best practices. By installing these extensions, you'll equip yourself with a powerful set of tools designed to enhance productivity and code quality.

Sometimes you need to reload the window for the changes to take effect. To do `Ctrl+Shift+P`, then type in `Reload Window` and select the option `Developer: Reload Window`

**Installed Extensions in the Extensions Tab**

<p align="center">
  <img src="/images/python_extensions.PNG" alt="Extensions Init screen" style="width: 100%;"/>
</p>



## 2. Test if you can run python. Create a Simple `test.py` Script and Running It

Let's see if we can run a basic python script!

- **Step 1:** Right-click in the Explorer window and select `New File`. Name it `test.py`.
- **Step 2:** Enter the following Python code:
  ```python
  print("Hello, World!")
  ```
- **Step 3:** Either click the play arrow in the right cornor or right-click in the editor and select `Run Python File in Terminal` to execute the script.

<p align="center">
  <img src="/images/test_script.PNG" alt="Extensions Init screen" style="width: 100%;"/>
</p>

If everything installed correctly, the terminal will pop up and you should see:

<p align="center">
  <img src="/images/test_1.PNG" alt="Test" style="width: 100%;"/>
</p>



## 3. Environment Management

### Creating a python virtual environment

Creating Python virtual environments for projects is crucial as it allows developers to manage dependencies and Python versions on a per-project basis. By isolating the project's environment, you ensure that each project has access to only the packages it needs, avoiding conflicts between package versions across different projects. This isolation enhances reproducibility, making it easier to share projects with others without worrying about mismatched dependencies. Furthermore, virtual environments facilitate smoother project setup and migration across different machines and platforms. By incorporating virtual environments into your workflow, you significantly improve project manageability and reduce the risk of issues related to package dependencies.

- **Step 1:** Open the integrated terminal (`Ctrl+``).
- **Step 2:** Run `python -m venv .venv` to create a virtual environment named `.venv`.
This will create a folder that will keep installed packages and the isolated python interpreter
- **Step 3:** We need to make sure VScode is using this interpreter as the default for this project. We can do this by clicking the button in the bottom right corner next the the notification. 
- **Step 4:** Now, whenever we run a python file it will use this interpreter

**Creating virtual environment**
<p align="center">
  <img src="/images/virtual_environment.PNG" alt="Virutal Enviornment" style="width: 100%;"/>
</p>

**Selecting default interpreter**
<p align="center">
  <img src="/images/virtual_environment_1.PNG" alt="Selecting default interpreter 1" style="width: 100%;"/>
</p>

**Selecting default interpreter**
<p align="center">
  <img src="/images/virtual_environment_2.PNG" alt="Selecting default interpreter 2" style="width: 100%;"/>
</p>

### Activate Virtual Environment and Install Libraries
For python environments, we must activate them and install the necessary packages

- **Step 1:** In the terminal, activate the virtual environment:
  - On Windows: `.venv\Scripts\activate`
  - On macOS/Linux: `source .venv/bin/activate`
- **Step 2:** Install libraries using pip:
  ```shell
  pip install matplotlib numpy pandas scipy
  ```

**Activate Virutal Environment**
<p align="center">
  <img src="/images/virtual_environment_activate.PNG" alt="Selecting default interpreter 2" style="width: 100%;"/>
</p>


## 4. Editing Code

In this section, We be going over some editing features.


### Autocomplete and IntelliSense
IntelliSense is a general term for code editing features that relate to code completion. 



##### 1. Linting example 
- **Step 1:** Create a new file called `linting.py`
- **Step 2:** Copy and paste the following into the file
```python
def greet(names):
    for name in names
    print "Hello, " + name + "!"

```


#### 3. Python Debugger

Python Debugger is Visual Studio Code extension that supports Python debugging with debugpy. Python Debugger provides a seamless debugging experience by allowing you to set breakpoints, step through code, inspect variables, and perform other essential debugging tasks. The debugy extension offers debugging support for various types of Python applications including scripts, web applications, remote processes, and multi-threaded processes.






## 6. A More Complicated Python File

- Create a new Python file named `complex_example.py` and demonstrate using functions and classes.

*Insert image and code example here*

## 7. One Dark Pro Extension

- Show how to install and apply the One Dark Pro theme from the Extensions view.

*Insert image here showing the theme*

## 8. AutoDocstring Extension

- Demonstrate using AutoDocstring to automatically generate docstrings for your functions and classes.

*Insert image showing the extension and its usage*

## 9. Jupyter Notebook Extensions

- Install the Jupyter extension and show how to create and use a Jupyter notebook within VS Code.

*Insert image showing a Jupyter notebook in VS Code*

## 10. Other Useful Extensions

- Briefly showcase other extensions like Auto Close Tag, Auto Rename Tag, Markdown All in One, PDF Viewer, Rainbow CSV, and HTML CSS Support.

*Insert images demonstrating these extensions*

## 11. Git Integration

- Initialize a git repository in your project folder and demonstrate basic git operations like commit and push.

*Insert image showing git operations*

