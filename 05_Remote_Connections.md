# Working with Remote SSH in Visual Studio Code

Visual Studio Code (VS Code) provides powerful capabilities for remote development through the Remote - SSH extension. This feature allows developers to connect to and work within remote environments directly from their local VS Code instance. This section demonstrates how to set up and use Remote SSH to connect to a High-Performance Computing (HPC) system, such as those provided by West Virginia University (WVU), and how to edit your SSH config file for easy access.

## Setting Up Remote SSH

### Installing the Remote - SSH Extension

1. Open VS Code.
2. Navigate to the Extensions view by clicking on the square icon on the sidebar or pressing `Ctrl+Shift+X`.
3. Search for "Remote - SSH" and click on the install button.

### Configuring SSH Connections

To connect to a remote HPC system via SSH, you must first configure your SSH connections by editing the `.ssh/config` file on your local machine. Here's how your config file might look based on the provided example:

```ssh
Host ssh.wvu.edu
  HostName ssh.wvu.edu
  ForwardX11Trusted yes
  User {YOUR USERNAME HERE}

Host tf.hpc.wvu.edu
  HostName tf.hpc.wvu.edu
  ForwardX11Trusted yes
  User {YOUR USERNAME HERE}
  ProxyCommand ssh {YOUR USERNAME HERE}@ssh.wvu.edu -W %h:%p

Host spruce.hpc.wvu.edu
  HostName spruce.hpc.wvu.edu
  ForwardX11Trusted yes
  User {YOUR USERNAME HERE}
  ProxyCommand ssh {YOUR USERNAME HERE}@ssh.wvu.edu -W %h:%p

Host ds.hpc.wvu.edu
  HostName ds.hpc.wvu.edu
  ForwardX11Trusted yes
  User {YOUR USERNAME HERE}
  ProxyCommand ssh {YOUR USERNAME HERE}@ssh.wvu.edu -W %h:%p
```

This configuration defines several HPC systems available at WVU, setting up direct connections and proxy commands as needed.

>> **Note:** If `.ssh/config` is not there create it. For windows `C:\Users\{YOUR_USER}\.ssh`. For Linux: `home/.ssh`.
This can also be accessed in VSCode by selecting `Configure SSH Hosts` After Step 2 of the next section.

### Connecting to Remote Connection in VS Code

After configuring your SSH connections:

1. Click the lower box in the corner. Hovering over it will say `Open a Remote Window`
2. Click on `Connect to Host...`
3. Choose the desired HPC system from the list of configured hosts (e.g., `tf.hpc.wvu.edu`).
4. Once you are connecting, you can open any folder on the explorer. You may need to go through the login process again.
5. You can connect to multiple login node by opening new terminals.

By following these steps, you can efficiently connect to remote HPC systems through SSH directly from VS Code, leveraging the Remote - SSH extension for seamless remote development. This setup allows you to edit files, run commands, and interact with your remote environment as if you were working locally, providing a powerful tool for developers who need to work with remote systems.