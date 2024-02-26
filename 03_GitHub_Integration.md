# Github Integration: Using Source Control in VSCode

VSCode integrates seamlessly with Git, allowing you to initialize repositories, make commits, and manage your code versions directly within the editor. Here's a concise guide on how to initialize a GitHub repository and create your first commit using VSCode's Source Control.


>> **Additional Information:** More information on git integration with vscode can be found here: **`https://code.visualstudio.com/docs/sourcecontrol/overview`**

## Setup

### Step 1: Install Git

Ensure Git is installed on your system. You can download it from [git-scm.com](https://git-scm.com/) and follow the installation instructions for your operating system.

### Step 2: Open Your Project in VSCode

- Launch VSCode.
- Open the folder where your project is located or where you want to create a new project.

### Step 3: Sign in to GitHub

- If you want to push your repository to GitHub, sign in to your GitHub account through VSCode when prompted. 

You need to install the **`GitHub Pull Requests`** extension if it's not already installed.

### Step 4: Configuring User Information

- Open the terminal

- Configure your name globally with the command: `git config --global user.name "Your Name"`

- Configure your name globally with the command: `git config --global user.email "your_email@example.com"`

- Verify Configuration with the command `git config --list`


>> **Note:** You may need to set up ssh-keys on your github account

## Initializing and Publishing on Github

### Step 1: Initialize a Repository

- Open the Source Control panel by clicking on the Source Control icon in the Activity Bar on the side of the window, or press `Ctrl+Shift+G` (`Cmd+Shift+G` on macOS).
- Click on `Initialize Repository`. If your folder is not yet a Git repository, VSCode will prompt you to initialize it. Confirm the action.


### Step 2: Make Your First Commit

- After initializing, any file changes will appear in the Source Control panel. Stage your changes by clicking the `+` icon next to each file or right-click and select `Stage Changes`.
- Enter a commit message in the input box at the top of the Source Control panel.
- Press `Ctrl+Enter` (`Cmd+Enter` on macOS) to commit the staged changes.

### Step 3: Publish to GitHub

- After committing your changes locally, click on the `...` button in the Source Control panel, go to `Remote`, and select `Publish to GitHub`.
- Follow the prompts to create a new repository on GitHub and push your commit.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/96b55ed8-d8fa-4d8a-874f-92bc8e9c777f

## Cloning a Github repository

Cloning a GitHub repository into Visual Studio Code (VSCode) allows you to work on projects from your local machine with ease. 

### Step 1: Find the repository to clone

- Navigate to the Github page of the repository to be cloned
- Click on the `Code` button and copy the URL provided.


### Step 2: Open Your Project in VSCode

- Launch VSCode.
- Open the explorer tab and press the `Clone Repository`

### Step 3: Find the repository to clone

- Navigate to the Github page of the repository to be cloned
- Click on the `Code` button and copy the URL provided.
- Paste the URL in the dialogue provided.

https://github.com/lllangWV/Python_Development_VScode/assets/120115419/5b295f81-992b-4384-b6db-7db83242dfb1


## Creating a New Branch

Creating a new branch in your repository allows you to work on new features or fixes without affecting the main codebase. Here's how to create a branch in Visual Studio Code (VSCode).

### Step 1: Creating the branch

- Open VSCodes for a project published on GitHub
- In the lower left corner, click the on the button `master`
- A dialogue box should pop up. Click `Create a Branch`
- Name the branch `feature`

### Step 2: Switch to the New Branch

- After creating the new branch, VSCode will automatically switch to it. You can start working on your changes in this new branch.
- You will know you are on the branch if the button in the lower left corner has your branch name `feature`.

### Step 3: Switching back to the master Branch

- To switch back, in the lower left corner, click the on the button `feature`
- A dialogue box should pop up. Click `master`

*Insert a placeholder for an image showing the branch creation process*

## Merging a Feature Branch into the Main Branch

Merging a feature branch into the main branch is a crucial step in collaborative development, allowing you to integrate new features or changes into the primary codebase. This section demonstrates how to perform this merge in Visual Studio Code (VSCode) and how to utilize the 3-way merge editor to resolve any conflicts that arise.

### Setup 
Before demonstrating how to merge a feature branch into the main branch and resolve conflicts using the 3-way merge editor in Visual Studio Code (VSCode), we need to set up a scenario where a merge conflict is guaranteed. This setup involves making changes on both the feature branch and the main branch that will conflict with each other.


#### Step 1: Make Changes in the Feature Branch
- On the `feature` branch, open or create a file where you'll make changes related to your feature.
- Make your changes and commit them to the feature-branch.
- Example change: Add a new function or modify an existing one in a way that it will conflict with changes on the main branch

#### Step 2: Making Conflicting Changes on the Main Branch

- In the same file you edited in the feature-branch, make different changes that will conflict with those made in the feature-branch.
- Commit these changes to the main branch.


By following these steps, you've now set up a scenario where merging the `feature`-branch into the `master` branch will result in a merge conflict. This setup is essential for demonstrating how to effectively use the 3-way merge editor in VSCode to resolve such conflicts.



### Step 1: Switch to the Main Branch

Before you can merge your feature branch, you need to switch to the branch you want to merge into, typically the main branch.

- Launch VSCode.
- Open the Source Control panel by clicking on the Source Control icon on the sidebar or pressing `Ctrl+Shift+G`.
- At the bottom left corner of VSCode, click on the current branch name to open the branch menu.
- Select the main branch (or the branch you wish to merge into) from the list to switch to it.

### Step 2: Merge the Feature Branch

With the main branch checked out, you're ready to merge your feature branch.

- Open the integrated terminal in VSCode by pressing ``Ctrl+` ``.
- Type `git merge feature-branch-name`, replacing `feature-branch-name` with the name of your feature branch, and press `Enter`.

### Step 3: Resolve Merge Conflicts with the 3-Way Merge Editor

If there are any conflicts during the merge, VSCode will alert you and provide tools to resolve them using the 3-way merge editor.

- Conflicted files will be listed in the Source Control panel. Click on a conflicted file to open it in the merge conflict editor.
- The editor will display three versions of the conflicted file: **Base** (common ancestor of the changes), **Incoming** (changes from the feature branch), and **Current** (changes in the main branch).
- Use the controls provided by VSCode to accept the incoming change, accept the current change, or manually edit the file to resolve the conflict.
- After resolving all conflicts in a file, save the file.
- Repeat this process for all conflicted files.
- Once all conflicts are resolved, complete the merge by staging the resolved files and committing them.

### Step 4: Finalize the Merge

After resolving all conflicts and staging the changes, commit the merge to finalize the integration of the feature branch into the main branch.

- In the integrated terminal, type `git commit` to commit the merge. You can include a commit message to describe the merge, such as "Merging feature-branch-name into main."

*Insert a placeholder for an image showing the 3-way merge editor and the process of resolving conflicts*

By following these steps, you can smoothly merge feature branches into the main branch, leveraging VSCode's 3-way merge editor to resolve conflicts efficiently. This process ensures that your main branch remains up-to-date with all the latest features and fixes, facilitating a collaborative and efficient development workflow.

## Extra Features

