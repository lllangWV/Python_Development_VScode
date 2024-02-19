
# Project in VS Code

We will be going over a demonstration of a Python Project in VScode. Throughout this demonstration I will be showing off the features be nice to have when developing

## 1. Opening and Creating a New Folder for the Python Project

- **Step 1:** Open VS Code.
- **Step 2:** Go to `File` > `Add Folder to Workspace...` and create a new folder named `vscode_demo`.
- **Step 3:** Open the new folder in VS Code to start your project.

*Insert image here showing the folder creation process*

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


## 3. Create a Python Virtual Environment

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

## 4. Activate Virtual Environment and Install Libraries

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


## 5. basic Python Extensions (Pylance, Python, Python Debuugger)

- Install essential Python extensions like Pylance, Python, and Python debugging by searching for them in the Extensions view (`Ctrl+Shift+X`) and clicking `Install`.

**Activate Virutal Environment**
<p align="center">
  <img src="/images/basic_python_extensions.PNG" alt="Selecting default interpreter 2" style="width: 100%;"/>
</p>

Sometimes you need to reload the window for the changes to take effect. To do `Ctrl+Shift+P`, then type in `Reload Window` and select the option `Developer: Reload Window`


### 1. Python

Python extension gives the following features
Pylance gives the following features
- **IntelliSense (Pylance)**
- **linting**
- **debugging (Python Debugger)**
- **code navigation**
- **variable explorer**
- **refactoring**
- **Code outline**

**Python extension page**

<p align="center">
  <img src="/images/python_extension.PNG" alt="Python extension" style="width: 100%;"/>
</p>

#### Linting example:


<video width="800" height="400" controls autoplay muted>
  <source src="/videos/python_linting_video.mp4" type="video/mp4">
</video>

### 2. Pylance

Pylance gives the following features
- **Docstrings**
- **Signature help, with type information**
- **Parameter suggestions**
- **Code completion**
- **Auto-imports (as well as add and remove import code actions)**
- **As-you-type reporting of code errors and warnings (diagnostics)**
- **Code outline**
- **Code navigation**
- **Type checking mode**
- **Native multi-root workspace support**
- **IntelliCode compatibility**
- **Jupyter Notebooks compatibility**
- **Semantic highlighting**


**Pylance extension page**

<p align="center">
  <img src="/images/pylance.PNG" alt="Pylance Extension" style="width: 100%;"/>
</p>


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

