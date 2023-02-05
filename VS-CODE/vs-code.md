# Installation
> See the [Download Visual Studio Code](https://code.visualstudio.com/download) page for a complete list of available installation options.

## Debian and Ubuntu based distributions

The easiest way to install Visual Studio Code for Debian/Ubuntu based distributions is to download and install the [.deb package (64-bit)](https://go.microsoft.com/fwlink/?LinkID=760868), either through the graphical software center if it's available, or through the command line with:

```python
sudo apt install ./<file>.deb

# If you're on an older Linux distribution, you will need to run this instead:
# sudo dpkg -i <file>.deb
# sudo apt-get install -f # Install dependencies
```

> Note that other binaries are also available on the [VS Code download page](https://code.visualstudio.com/Download).

Installing the .deb package will automatically install the apt repository and signing key to enable auto-updating using the system's package manager. Alternatively, the repository and key can also be installed manually with the following script:

```python
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
```
Then update the package cache and install the package using:

```python
sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders
```

> Detail info at: [VS CODE HELP PAGE](https://code.visualstudio.com/docs/setup/linux)


---

<p>&nbsp;</p>

# Uninstall Visual Studio Code
The steps for uninstalling Visual Studio Code will depend on your platform (Windows, macOS, or Linux) and the install option that you used. For example on Windows, you can use the System or User Windows Installers or download a .zip file and extract the contents anywhere on your machine.

In general, you would uninstall VS Code as you would any other desktop application and follow your platform's recommended flow for uninstalling software. Specific platform guidance is provided below as well as how to completely clean up any remaining VS Code configuration files.

<p>&nbsp;</p>

# Windows
## Windows Installer
If you installed VS Code via the Windows Installer, either the User or System version, use the installer to remove VS Code.

- Start menu
- - Search for **Add or Remove Programs** and find Visual Studio Code in the Apps > Apps & features list.
- - Select Uninstall from the actions dropdown on the right side (three vertical dots).
- - Follow the prompts to uninstall VS Code.
- Control Panel
- - Under Programs, select the Uninstall a program link.
- - Find the Visual Studio Code entry, right-click, and select the Uninstall command.
- - Follow the prompts to uninstall VS Code.

## .zip file installation
If you installed VS Code on Windows by downloading and extracting one of the ```.zip``` files, you can uninstall by deleting the folder where you extracted the ```.zip``` contents.

<p>&nbsp;</p>

# macOS
To uninstall VS Code on macOS, open Finder and go to Applications. Right-click on the Visual Studio Code application and select Move to Trash.

Linux
To uninstall VS Code on Linux, you should use your package manager's uninstall or remove option. The exact command line will differ depending on which package manager you used (for example, ```apt-get```, ```rpn```, ```dnf```, ```yum```, etc.).

The names for the VS Code packages are:

- code - VS Code Stable release
- code-insiders - VS Code Insiders release

For example, if you installed VS Code via the Debian package (.deb) and apt-get package manager, you would run:

```shell
sudo apt-get remove code
```

where ```code``` is the name of the VS Code Debian package.

<p>&nbsp;</p>

# Clean uninstall
If you want to remove all user data after uninstalling VS Code, you can delete the user data folders ```Code``` and ```.vscode```. This will return you to the state before you installed VS Code. This can also be used to reset all settings if you don't want to uninstall VS Code.

The folder locations will vary depending on your platform:


- Windows - ```Delete %APPDATA%\Code and %USERPROFILE%\.vscode.```
- macOS - ```Delete $HOME/Library/Application Support/Code and ~/.vscode.```
- Linux - Delete ``` $HOME/.config/Code and ~/.vscode.```