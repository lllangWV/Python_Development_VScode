
# Setting up VS Code for python development

## Installing VSCode

Visual Studio Code is a free, open-source editor that supports a wide range of programming languages and frameworks. To download and install it, follow these steps:

1. Go to the [Visual Studio Code official website](https://code.visualstudio.com/).
2. Click on the download button for your operating system (Windows, macOS, or Linux).
3. Once the download is complete, run the installer and follow the on-screen instructions to install VS Code.
## Installing Git

Git is a powerful version control system widely used for software development and other version control tasks. Here's a concise guide to installing Git on Windows, macOS, and Linux systems.

## Windows

1. **Download the Installer**: Visit the [Git website](https://git-scm.com/) and download the latest version of Git for Windows. The download should automatically suggest the best version for you.

2. **Run the Installer**: Open the downloaded `.exe` file and follow the installation prompts. Default settings are typically sufficient for most users, but you can customize the installation options according to your needs.

3. **Verify Installation**: Open the Command Prompt or Git Bash (installed with Git) and type `git --version` to check if Git was installed successfully.

## macOS

### Homebrew

If you have Homebrew installed, you can install Git by opening a terminal and running:

```bash
brew install git
```

### Installer

1. **Download the Installer**: Visit the [Git website](https://git-scm.com/download/mac) and download the latest version of Git for macOS.

2. **Run the Installer**: Open the downloaded `.dmg` file, and follow the installation prompts to install Git.

3. **Verify Installation**: Open the Terminal and type `git --version` to ensure Git is installed correctly.

## Linux

### Debian/Ubuntu

Open a terminal and run:

```bash
sudo apt-get update
sudo apt-get install git
```


```

## Verify Installation

Regardless of your operating system, you can verify the installation by opening a terminal (or Command Prompt on Windows) and running:

```bash
git --version
```

This command should return the installed version of Git, confirming it was successfully installed.

## Configuring Git

After installing, it's a good practice to set up your user name and email address since Git uses these details in your commit transactions. Open a terminal or Command Prompt and run the following commands, replacing the placeholders with your information:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

You're now ready to start using Git for your version control needs.


## Downloading and Installing Python

### Through python.org
To download and install Python, follow these steps:

1. Navigate to the official Python website at [python.org](https://www.python.org/).
2. Hover over the "Downloads" tab. The website will usually detect your operating system and display the recommended version for you to download. If it doesn't, you can manually select your OS from the available options.
3. Click on the download link for the latest Python version. As of my knowledge cutoff in April 2023, Python 3.10 is the latest stable release.
4. Once the installer is downloaded, open it to begin the installation process.
5. In the installer, make sure to check the box that says "Add Python 3.x to PATH" before you click "Install Now". This step is crucial as it makes Python accessible from the command line.
6. Follow the on-screen instructions to complete the installation.

After the installation is complete, you can verify that Python is installed correctly by opening your command-line interface (CLI) and typing `python --version`. You should see the version of Python that you installed displayed in the terminal.

With Python installed, you're ready to set up Visual Studio Code for Python development.

> **Note:** If you're using a Linux distribution, Python is likely already installed on your system. You can check by typing `python3 --version` in your terminal. If it's not installed, you can use your distribution's package manager to install Python.

### Through anaconda.com

Anaconda is a popular distribution of Python that includes many of the libraries and tools commonly used in data science, machine learning, and scientific computing. It's an excellent way to manage Python packages and environments, especially for those who work on complex projects with specific library versions. Here's how you can set up Python through Anaconda:


1. Visit the Anaconda distribution page at [anaconda.com](https://www.anaconda.com/products/distribution).
2. Click on the "Download" button to go to the download section.
3. Choose the appropriate installer for your operating system. Anaconda is available for Windows, macOS, and Linux.
4. Select the Python 3.x version since it's the most up-to-date and widely used.
5. After downloading the installer, run it to start the installation process.
6. Follow the installer's prompts. Make sure to agree to the license terms and add Anaconda to your PATH environment variable. While adding it to PATH is not required due to the Anaconda Navigator and Anaconda Prompt, some users prefer direct access from their terminal.
7. Complete the installation by following the on-screen instructions.

### Verifying the Installation

To ensure that Anaconda is installed correctly:

1. Open the Anaconda Navigator, a graphical user interface that comes with Anaconda, by searching for it in your applications menu or using the command line by typing `anaconda-navigator`.
2. You can also use the command line to verify the installation. Open your terminal (or Anaconda Prompt on Windows) and type `conda --version`. You should see the version of conda that was installed.
3. To verify that Python has been installed, type `python --version` or `conda list`. This will show the Python version installed by Anaconda as well as a list of installed packages.

With Anaconda installed, you can create isolated Python environments to manage dependencies for different projects, install packages, and launch applications like Jupyter Notebook.

### Managing Python Environments with Conda



## Installing the Python Extension for VS Code

VS Code has an extensive library of extensions that enhance its functionality. For Python development, you'll need to install the official Python extension.

1. Open VS Code.
2. Navigate to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window.
3. Search for 'Python' in the Extensions view search bar.
4. Find the Python extension authored by Microsoft (usually the first result) and click on the Install button.


