---
title: Setup
weight: 20
---

# Setup
To get your computer ready, we need to configure the workspace you will use for the class.


{{< tabs "computer-setup" >}}
{{< tab "MacOS" >}}
## Install software
1. Start your Terminal application (you can find it in your applications or using Spotlight search).
1. Run the software installation script by pasting the following line into the window that opens
and pressing `return`. Enter your computer's password when the window prompts you (you won't see
any text when you're typing but that's ok).

```shell
bash <(curl -sL https://raw.githubusercontent.com/wolfj95/mims-setup/main/setup_script_mac.sh)
```

You can test out the
setup by opening a new Terminal window and running the following command:
```shell
jupyter notebook
```

This should open a window in your web browser displaying the Jupyter interface.

{{< /tab >}}

{{< tab "Windows" >}}

## Install Windows Terminal and Python3
1. Download the Windows Terminal application to your computer. You can [download it
from the Microsoft Store](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab).
1. Open the Windows Terminal application.
1. In the window that opens, type `python` and press enter. This should open the Microsoft Store page for Python 3.9.
1. Download and install Python 3.9 from the Microsoft store. [Note: If you already have Python 3.7 or higher installed
on your computer, you don't need to upgrade Python.

After the installation is complete, return to the Windows Terminal and enter the following command: `python --version`.
This should output `Python 3.9.6` (or whatever version of Python you have above 3.7).

## Install Jupyter
0. In a Windows Terminal window, install the Jupyter python package using the following command: `pip install jupyter`.
This will install a variety of packages needed to run the coding environment we'll use for this  course.

Test that Jupyter is correctly installed by running the command: `python -m notebook`. This will start a server and open
a Jupyter notebook page in your web browser. You may need to click on the URL provided in the Terminal window if the page
does not load.

## Install git
1. Download [Git for Windows](http://git-scm.com/download/win).
1. Open the file you downloaded and allow the program to make changes
to your device.
1. Answer the prompts in the installer choosing the default setting for each prompt.

To test your git installation, return to the Windows Terminal window. **Restart the Windows Terminal** and type the following
command: `git --version`. This should output `git version 2.32.9.windows.2` (or a higher version).

## Done!
Congrats your computer is now ready for the course!

{{< /tab >}}
{{< /tabs >}}

{{< expand "Something isn't right..." >}}

{{< tabs >}}
{{< tab "Mac Help" >}}
If the script shows that there were errors, there may be a problem with your setup.

You can try installing each piece of software individually (rather than all at once
using the script). The sections below describe how to install each piece of software
needed for the course.

### Install Xcode
You need Xcode Command Line Tools in order to run Homebrew and install Python.

Your can install it in the Terminal by using this command and following the prompts:
```shell
xcode-select --install
```

However, if you're having problems with the download, you can also download the software
from [the Apple Developer website](https://developer.apple.com/download/all/). Select `Command
Line Tools for Xcode 13 beta 4`.

After the install, running the command `xcode-select --install` in your Terminal should produce
the message: `xcode-select: error: command line tools are already installed, use "Software Update" to install updates`.

### Install Homebrew
Homebrew is the package manager we use to install Python3 and git. You can install Homebrew by
running the following command in your terminal:
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

You can test this installation by running the following command and making sure that it outputs
a version number:
```shell
brew --version
```

### Install Brew packages
Now, you can use Homebrew to install packages. Run the following commands to install Python3:

```shell
brew install python3
```

You can test this installation by running the following command and making sure that it outputs
a version number:
```shell
python3 --version
```

Then, install git:
```shell
brew install git
```

And test using:
```shell
git --version
```

### Install Jupyter
Jupyter notebooks is the programming environment we'll use for the course. You can install
it with the Python package installer, pip, using the following command:

```shell
pip3 install jupyter
```

### Oops
If you're still having problems while following the steps above, [contact an instructor]({{< ref "contact" >}}).

{{< /tab >}}

{{< tab "Windows Help" >}}
If you run into a problem while following the steps above, [contact an instructor]({{< ref "contact" >}}).
{{< /tab >}}

{{< /tabs >}}

{{< /expand >}}
