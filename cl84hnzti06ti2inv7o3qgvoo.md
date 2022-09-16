## How to set up a developer environment on Mac and PC

The hardest part of becoming a software engineer is starting. New developers may feel overwhelmed with everything they have to learn and never take the first step.

Before writing a line of code every developer needs to first set up their dev environment. This article is to help non-devs dip their toes into the world of software development by providing an easy to follow step by step guide to set up every tool you need to start coding.

I guarantee this will be the simplest introduction to development on the internet and that anyone will be able to follow this guide. 

## Developer environment setup for Windows
To code on a windows device, you will need to download a Linux subsystem. This sounds much more daunting than it actually is. This is completely free and easy to set up. 

You must have at least Windows 10 or higher to be able to set this up.

Microsoft has a really great guide [here](https://docs.microsoft.com/en-us/windows/wsl/install) that you can follow. I will provide the same guide with pictures so you can follow along.

### Setting up Windows Subsystem for Linux (WSL)
1. In your application bar search for "PowerShell" and run this application as an administrator.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663295216169/b9HCy_B2K.png align="center")
2. There should be a blue PowerShell terminal that opens up. Copy and paste this into the terminal and press enter:
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663295338105/hO-FXlOQW.png align="center")
3. After this command finishes running restart your computer.
4. In your application bar search for "Microsoft Store" and open the application.
5. Find "Ubuntu" in the Microsoft Store and click "Get" then "Install"
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663295494996/jnR1f9tD9.png align="center")
6. It will install some files and then prompt you to "Enter new UNIX username", enter a username, and then it will prompt you for a password for your new user.
7. Once you have your user, this command which should update all your packages:
```
sudo apt update
```
8. Once that is done upgrade your packages by running:
```
sudo apt upgrade
```
9. Next you have to configure Git by setting your git user name by running:
```
git config --global user.name "Your Name"
```
You should replace "Your Name" with your name.
10. Next configure Git to use your email, you should use the email associated with your GitHub account:
```
git config --global user.email youremail@email.com
```
Replace "youremail@email.com" with your email.

### Installing and configuring Visual Studio Code (VSCode)
1. You will need to install Visual Studio Code, you can do that by going to the [VSCode website](https://code.visualstudio.com/download) and clicking download for Windows.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663303164811/VzsoFyr99.png align="center")
2. Once VSCode is done installing open it and it should prompt you to install "Remote - WSL" since you have Window Linux Subsystem installed on your system. Click install.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663303287512/rMbLNSZFo.png align="center")
3. After it is done downloading close VSCode.
4. Open Ubuntu and run this to open VSCode from the command line:
```
code .
```
This will install VSCode Server and open VSCode.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663303786107/5HXfrXkIG.png align="center")
5. You can use this method to open your VSCode or just search for the application in your application bar and run it.
6. That's it! You're all set up to start coding on your new code editor on a Window Subsystem for Linux.

## Developer environment setup for Macs
To start coding on a Mac you have to download a few things. Instead of setting up a Linux subsystem like what we had to do on Windows, we will have to use Homebrew to use the command line to install software and tools. 

### Installing Homebrew
Homebrew allows you to download applications and tools. It is a package manager for Macs that simplifies installing software on macOS. You can check their website out [here](https://brew.sh/). It is open-source and 100% safe as long as you know what you're downloading with it. 

1. Open your terminal.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663304614384/f2u5-LJry.png align="center")
2. Run this command to install Homebrew:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
You will be prompted to continue or abort. Press `RETURN` to continue. 

### Using Homebrew to install Git
1. Install git using Homebrew by running:
```
brew install git
```
2. Configure your git by setting your username:
```
git config --global user.name "Your Name"
```
You should replace "Your Name" with your name.
10. Next configure Git to use your email, you should use the email associated with your GitHub account:
```
git config --global user.email youremail@email.com
```
Replace "youremail@email.com" with your email.

### Install Virtual Studio Code
You can go to [Virtual Studio Code's website](https://code.visualstudio.com/download) and click download for Mac. You should be able to unzip it and drag it into your applications. That's it, now you can start coding!
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663305348484/MLqDocPnq.png align="center")

## Conclusion
Once you have these basic tools set up on your computer you will be ready to start coding whatever you like. You can always download more tools and software. For example, if you wanted to start doing Ruby development you could install rbenv and Ruby using Homebrew or WSL. 

If you are a complete beginner starting to learn how to code I would recommend checking out my beginner developer series. The next article you should read is the [How to use Git and GitHub article](https://www.blog.edmondhui.com/how-to-use-git) now that you have set up your development environment and are ready to start committing code.


![Thank you for Reading.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663306568906/pSzuDzRNG.png align="left")
