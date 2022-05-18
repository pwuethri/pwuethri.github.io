---
title: "How to install WSL on Windows"
date: 2022-05-17
showToc: false
TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowRssButtonInSectionTermList: true
draft: False
tags: [Tutorial, WSL, Linux]
---

# Introduction

Windows Subsystem Linux (WSL) is an amazing feature that allows users to run full Linux distros directly from Windows. It removes the need to run a virtual machine or restart and select an OS during dualbooting. 

In this post, we will see how easy it is to install WSL on Windows and get an Ubuntu distribution up and running.

# Installing WSL

Installing WSL can be done by running __Powershell__ (as an administrator) and run the command 
```
wsl --install
```

This will actually install Ubuntu by default. To change this, we could use the command 
```
wsl --install -d <Distribution Name>
```

The list of available distributions can be seen with `wsl --list --online` (equivalent to `wsl -l -o`!). 

There are two versions of WSL, and this will set WSL2 as the default. We can use the command `wsl -l -v` in powershell or Windows command prompt to check which version is currently being used. If we would like to switch, `wsl --set-default-version <1/2>` will do the trick.

# Setting up Linux

Running the __Ubuntu__ app will open a window which will prompt us to enter an username and password. This will become the default user whenever Ubuntu is launched.

One nifty trick is to link the Windows home folder to Linux's home folder via a symbolic link `ln -s /mnt/c/Users/<username> ~/winhome`. This will make the access to the Windows files easy via the command `cd ~/winhome`.

Packages can be updated and upgraded as usual via `sudo apt update && sudo apt upgrade`.

# Setting up Windows Terminal

Windows Terminal is a great app to access and customize applications which have a command line interface. The Terminal can be downloaded directly from the Microsoft Store. 

# Resources

- WSL documentation: [https://docs.microsoft.com/en-us/windows/wsl/](https://docs.microsoft.com/en-us/windows/wsl/)
- Link to Windows files: [https://unix.stackexchange.com/questions/658031/how-do-i-make-a-shortcut-to-a-path-using-two-tilde-characters-or-similar](https://unix.stackexchange.com/questions/658031/how-do-i-make-a-shortcut-to-a-path-using-two-tilde-characters-or-similar)
