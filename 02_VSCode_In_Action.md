
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

- **Step 1:** Open the integrated terminal **Ctrl+`**.
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

### Final Thoughts

- Conda environments will also automatically be detected


## 4. Editing Code

In this section, We be going over some editing features.


### Autocomplete and IntelliSense
IntelliSense is a general term for code editing features that relate to code completion. When print is typed, notice how IntelliSense populates auto-completion options. The user is also given a list of options when they begin to type the variable named greeting. 

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/b095e5c8-13db-4de9-b80d-fe1eb8733688

Autocomplete and IntelliSense are provided for all files within the current working folder. They're also available for Python packages that are installed in standard locations.

### Enable Auto Imports

Pylance offers auto import suggestions for modules in your workspace and/or packages you have installed in your environment. This enables import statements to be automatically added as you type. Auto imports are disabled by default, but you can enable them by setting `python.analysis.autoImportCompletions` to `true` in your settings.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/2e203a60-31f6-4050-b3f5-238c66692a39

The settings can be found in `File->Preferences->Settings`. Once the settings tab is open, use the search base to fine the above setting.

### Navigation

While editing, you can right-click different identifiers to take advantage of several convenient commands

- **Go to Definition** (`F12`) jumps from your code into the code that defines an object. This command is helpful when you're working with libraries.

- **Peek Definition** (`Alt+F12`), is similar, but displays the definition directly in the editor (making space in the editor window to avoid obscuring any code). Press `Escape` to close the Peek window or use the **x** in the upper right corner.

- **Go to Declaration** jumps to the point at which the variable or other object is declared in your code.

- **Peek Declaration** is similar, but displays the declaration directly in the editor. Again, use `Escape` or the **x** in the upper right corner to close the Peek window

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/75057ef5-035a-47b3-9650-efe53204385c

**Starting code**
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import savgol_filter

# Generate a sine wave
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Introduce some noise
noise = np.random.normal(0, 0.1, y.shape)
noisy_signal = y + noise

# Attempt to smooth the noisy signal
# Intentional mistake: window length is even; it should be odd
window_length = 24  # This should be an odd number
polynomial_order = 3
try:
    smoothed_signal = savgol_filter(noisy_signal, window_length, polynomial_order)
except ValueError as e:
    print(f"Error encountered: {e}")
    # Placeholder for corrected window_length, for demonstration
    window_length = 25
    smoothed_signal = savgol_filter(noisy_signal, window_length, polynomial_order)

# Plotting
plt.figure(figsize=(10, 6))
plt.plot(x, y, label='Original Sine Wave')
plt.plot(x, noisy_signal, label='Noisy Signal')
plt.plot(x, smoothed_signal, label='Filtered Signal')
plt.legend()
plt.show()
```

### Refactoring 
The Python extension adds the following refactoring functionalities: Extract Variable, Extract Method and Rename Module. It also supports extensions that implement additional refactoring features such as Sort Imports.

- **Extract Variable**  Extracts all similar occurrences of the selected text within the current scope, and replaces it with a new variable. You can invoke this command by selecting the line of code you wish to extract as a variable. Then select the light-bulb or right click and select refactor.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/24cb6ca6-4ae7-4bc5-ab0d-5dd76fc3b156

**Starting code**
```python
def price_after_tax(price):
    return price + (price * 0.2)  # 20% tax
```

- **Extract Method**  Extracts all similar occurrences of the selected text within the current scope, and replaces it with a new variable.You can invoke this command by selecting the line of code you wish to extract as a variable. Then select the light-bulb or right click and select refactor.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/2c4fa26e-aabe-4c0f-8136-de0ec6a09a2d

**Starting code**
```python
def process_circle_data(radius_input):
    # Validate input
    if not isinstance(radius_input, (int, float)) or radius_input <= 0:
        print("Error: The radius must be a positive number.")
        return

    # Calculate area
    area = 3.14159 * radius_input ** 2

    # Calculate circumference
    circumference = 2 * 3.14159 * radius_input

    # Print results
    print(f"Circle with radius {radius_input}:")
    print(f"Area: {area}")
    print(f"Circumference: {circumference}")

```

- **Rename Module**  Extracts all similar occurrences of the selected text within the current scope, and replaces it with a new variable. You can invoke this command by selecting the line of code you wish to extract as a variable. Then select the light-bulb or right click and select refactor.

**Create file called `circle_lib.py`**
```python
def process_circle_data(radius_input):
    # Validate input
    if not isinstance(radius_input, (int, float)) or radius_input <= 0:
        print("Error: The radius must be a positive number.")
        return

    # Calculate area
    area = 3.14159 * radius_input ** 2

    # Calculate circumference
    circumference = 2 * 3.14159 * radius_input

    # Print results
    print(f"Circle with radius {radius_input}:")
    print(f"Area: {area}")
    print(f"Circumference: {circumference}")
    return area, circumference

```

**Create file called `main.py`**
```python
from circle_lib import process_circle_data

area, circumference = process_circle_data(10)
```


After a Python file/module is renamed, Pylance can find all instances that may need to be updated and provide you with a preview of all the changes.

To customize which references need to be updated, you can toggle the checkboxes at the line or from the file level in `Refactor Preview`. Once you've made your selections, you can select `Apply Refactoring` or `Discard Refactoring`.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/bec06ef9-866c-41d1-9d07-f3447cfbd8c9

## 5. Linting

Linting highlights semantic and stylistic problems in your Python source code, which often helps you identify and correct subtle programming errors or coding practices that can lead to errors. For example, linting can detect the use of an undefined variable, calls to undefined functions, missing parentheses, and even more subtle issues such as attempting to redefine built-in types or functions. Linting is distinct from Formatting because linting analyzes how the code runs and detects errors, whereas formatting only restructures how code appears.

>> **Note**: Syntax error detection is enabled by default in the Python extension's Language Server. To learn how you can configure the Language Server, see Language Server Settings. This document covers how you can enable linting for additional code detection, including stylistic checks.

**Starting code**
```python
def process_circle_data(radius_input):
    # Validate input
    if not isinstance(radius_input, (int, float)) or radius_input <= 0
    print("Error: The radius must be a positive number.")
    return

    # Calculate area
    area = 3.14159 * radius_input ** 2

    # Calculate circumference
    circumference = 2 * 3.14159  radius_input

    # Print results
    print f"Circle with radius {radius_input}:"
    print(f"Area: {area}")
    print(f"Circumference: {circumference}")

```

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/9c48382c-de31-4812-acc9-a0a26f582f03

## 6. Formating

Formatting makes source code easier to read by human beings. By enforcing particular rules and conventions such as line spacing, indents, and spacing around operators, the code becomes more visually organized and comprehensible. You can view an example on the autopep8 page. Keep in mind, formatting doesn't affect the functionality of the code itself.

**Starting code**
```python

from scipy.integrate import quad
def integrateFunction(x):

    return x**2
result, error = quad(integrateFunction, 0, 1)
print("Integration result:", result, "Error:", error)

import numpy as np
x = np.linspace(0, 10, 100)
y = np.sin(x)

import matplotlib.pyplot as plt
plt.plot(x, y)
plt.title("Sine Wave")
plt.xlabel("X")
plt.ylabel("Y")
plt.show()
```

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/d3221ff6-f297-42ae-b764-42abe4d6bf9b

### Python Debugging

VSCode's integrated debugging support allows developers to launch or attach to their running apps and debug with breakpoints, call stacks, and an interactive console. These capabilities make it an invaluable tool for developers seeking to quickly identify the root causes of issues without leaving their coding environment.

If you're only interested in debugging a Python script, the simplest way is to select the down-arrow next to the run button on the editor and select `Python Debugger: Debug Python File`.

**Starting code**
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import savgol_filter

# Generate a sine wave
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Introduce some noise
noise = np.random.normal(0, 0.1, y.shape)
noisy_signal = y + noise

# Attempt to smooth the noisy signal
# Intentional mistake: window length is even; it should be odd
window_length = 24  # This should be an odd number
polynomial_order = 3
try:
    smoothed_signal = savgol_filter(noisy_signal, window_length, polynomial_order)
except ValueError as e:
    print(f"Error encountered: {e}")
    # Placeholder for corrected window_length, for demonstration
    window_length = 25
    smoothed_signal = savgol_filter(noisy_signal, window_length, polynomial_order)

# Plotting
plt.figure(figsize=(10, 6))
plt.plot(x, y, label='Original Sine Wave')
plt.plot(x, noisy_signal, label='Noisy Signal')
plt.plot(x, smoothed_signal, label='Filtered Signal')
plt.legend()
plt.show()

```

#### Using the Debugger

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/6cf6d3a4-8326-4eee-a648-da45ad118f8d

#### Using Breakpoints in Debugging

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/c4819970-4cf3-43c3-9c45-687c54c9a88f

## 6. Customizing Shortcut Keys in VSCode

Visual Studio Code (VSCode) is a highly customizable editor, allowing you to tailor its functionality to suit your workflow. One common customization is changing shortcut keys. In this tutorial, we'll walk through how to change the shortcut for the "Comment All" action to `Ctrl+1`.

#### Step 1: Open Keyboard Shortcuts

- **Method 1: Using the Command Palette**
  - Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS) to open the Command Palette.
  - Type `keyboard shortcuts` and select `Preferences: Open Keyboard Shortcuts`.

- **Method 2: Using the Menu**
  - Go to `File` > `Preferences` > `Keyboard Shortcuts`. On macOS, it's `Code` > `Preferences` > `Keyboard Shortcuts`.

#### Step 2: Search for the Comment Command

- In the Keyboard Shortcuts interface, there's a search bar at the top. Type `comment` to filter out the relevant commands. You're looking for something along the lines of `Toggle Line Comment` or `Add Line Comment` and `Remove Line Comment`, depending on how VSCode phrases it in your version. These commands typically use `Ctrl+/` (Windows/Linux) or `Cmd+/` (macOS) by default.

#### Step 3: Change the Shortcut

- Once you've found the toggle comment command, click on the pencil icon next to it to edit.
- Press `Ctrl+1` (or `Cmd+1` on macOS) when prompted to enter the new keybinding. VSCode will then show `Ctrl+1` in the input field.
- Press `Enter` to save the new keybinding.

#### Step 4: Resolve Conflicts

- If `Ctrl+1` is already assigned to another command, VSCode will alert you to the conflict. You must decide whether to proceed (overriding the existing command) or choose a different combination.
- If you choose to override, the previous command assigned to `Ctrl+1` will no longer have that shortcut.

#### Step 5: Testing

- Open any file in your editor, select multiple lines of code, and press `Ctrl+1`. The lines should now be commented out. Pressing `Ctrl+1` again will uncomment them.
- If the shortcut doesn't work as expected, double-check the steps above to ensure everything was applied correctly.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/21775937-dd3d-4748-b366-1d9ba7c441d3

#### Additional Tips

- **Customize Further**: Explore and customize other shortcuts in the same Keyboard Shortcuts menu to enhance your productivity.
- **Use the JSON file for Advanced Customization**: For more advanced users, VSCode offers the option to edit keybindings directly in a JSON file. Access this by clicking the `{}` icon in the top right corner of the Keyboard Shortcuts tab.


## 7. Jupyter Notebook

Jupyter (formerly IPython Notebook) is an open-source project that lets you easily combine Markdown text and executable Python source code on one canvas called a **notebook**. Visual Studio Code supports working with Jupyter Notebooks natively, as well as through Python code files.

#### Create a jupyter notebook called `plot.ipynb`


**Starting code**
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import savgol_filter

# Generate a sine wave
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Introduce some noise
noise = np.random.normal(0, 0.1, y.shape)
noisy_signal = y + noise

# Attempt to smooth the noisy signal
# Intentional mistake: window length is even; it should be odd
window_length = 24  # This should be an odd number
polynomial_order = 3
try:
    smoothed_signal = savgol_filter(noisy_signal, window_length, polynomial_order)
except ValueError as e:
    print(f"Error encountered: {e}")
    # Placeholder for corrected window_length, for demonstration
    window_length = 25
    smoothed_signal = savgol_filter(noisy_signal, window_length, polynomial_order)

# Plotting
plt.figure(figsize=(10, 6))
plt.plot(x, y, label='Original Sine Wave')
plt.plot(x, noisy_signal, label='Noisy Signal')
plt.plot(x, smoothed_signal, label='Filtered Signal')
plt.legend()
plt.show()

```
https://github.com/lllangWV/Python_Development_VScode/assets/120115419/da2f03de-e049-4c6b-b2ac-10c942cbe8c2

## 7. Github Integration: Using Source Control in VSCode

VSCode integrates seamlessly with Git, allowing you to initialize repositories, make commits, and manage your code versions directly within the editor. Here's a concise guide on how to initialize a GitHub repository and create your first commit using VSCode's Source Control.

### Initializing and Publishing on Github

#### Step 1: Install Git

Ensure Git is installed on your system. You can download it from [git-scm.com](https://git-scm.com/) and follow the installation instructions for your operating system.

#### Step 2: Open Your Project in VSCode

- Launch VSCode.
- Open the folder where your project is located or where you want to create a new project.

#### Step 3: Sign in to GitHub

- If you want to push your repository to GitHub, sign in to your GitHub account through VSCode when prompted. 

You need to install the **`GitHub Pull Requests`** extension if it's not already installed.

#### Step 4: Configuring User Information

- Open the terminal

- Configure your name globally with the command: `git config --global user.name "Your Name"`

- Configure your name globally with the command: `git config --global user.email "your_email@example.com"`

- Verify Configuration with the command `git config --list`


#### Step 4: Initialize a Repository

- Open the Source Control panel by clicking on the Source Control icon in the Activity Bar on the side of the window, or press `Ctrl+Shift+G` (`Cmd+Shift+G` on macOS).
- Click on `Initialize Repository`. If your folder is not yet a Git repository, VSCode will prompt you to initialize it. Confirm the action.


#### Step 5: Make Your First Commit

- After initializing, any file changes will appear in the Source Control panel. Stage your changes by clicking the `+` icon next to each file or right-click and select `Stage Changes`.
- Enter a commit message in the input box at the top of the Source Control panel.
- Press `Ctrl+Enter` (`Cmd+Enter` on macOS) to commit the staged changes.

#### Step 6: Publish to GitHub

- After committing your changes locally, click on the `...` button in the Source Control panel, go to `Remote`, and select `Publish to GitHub`.
- Follow the prompts to create a new repository on GitHub and push your commit.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/96b55ed8-d8fa-4d8a-874f-92bc8e9c777f

### Cloning a Github repository

Cloning a GitHub repository into Visual Studio Code (VSCode) allows you to work on projects from your local machine with ease. 

#### Step 1: Find the repository to clone

- Navigate to the Github page of the repository to be cloned
- Click on the `Code` button and copy the URL provided.


#### Step 2: Open Your Project in VSCode

- Launch VSCode.
- Open the explorer tab and press the `Clone Repository`

#### Step 2: Find the repository to clone

- Navigate to the Github page of the repository to be cloned
- Click on the `Code` button and copy the URL provided.
- Paste the URL in the dialogue provided.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/5b295f81-992b-4384-b6db-7db83242dfb1

#### Extra Features

- **Additional Information:** More information on git integration with vscode can be found here: `https://code.visualstudio.com/docs/sourcecontrol/overview`
- **Branch management**
- **Merge conflict manager**


## 7. Other useful extenstions

- **One Dark Pro**: A comfortable dark theme for extended coding sessions.
- **Material Icon Theme**: Adds a rich set of icons to improve the visual grepping of your projects.
- **Markdown Preview Enhanced**: A powerful markdown extension with preview features.
- **autoDocstring**: Generate Python docstrings automatically.
- **Excel Viewer**: View Excel spreadsheets and CSV files within VS Code.
- **HTML CSS Support**: Autocomplete for HTML classes and IDs defined in your stylesheets.
- **Rainbow CSV**: Highlight CSV and TSV files in different colors for easier editing and visualization.
- **vscode-pdf**: View PDF files directly in VS Code.


#### AutoDoc example

**`AutoDoc`** is a powerful extension for Visual Studio Code (VSCode) designed to streamline the documentation process for your code. By automatically generating docstrings for your functions and classes, AutoDoc helps maintain clear and consistent documentation, improving readability and maintainability.

**Starting Code**
```python
def merge_and_analyze_lists(primary_list, secondary_list, sort=True, reverse=False):
    if not isinstance(primary_list, list) or not isinstance(secondary_list, list):
        raise ValueError("Both arguments must be of type 'list'")
    
    merged_list = primary_list + secondary_list
    
    if sort:
        merged_list = sorted(merged_list, reverse=reverse)
    
    total_elements = len(merged_list)
    unique_elements = len(set(merged_list))
    first_element = merged_list[0]
    last_element = merged_list[-1]
    
    return {
        'total_elements': total_elements,
        'unique_elements': unique_elements,
        'first_element': first_element,
        'last_element': last_element
    }
```

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/914cc58b-704a-4eb3-888a-509370514618

