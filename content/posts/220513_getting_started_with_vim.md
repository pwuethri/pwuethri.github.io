---
title: "Setting up a Coding Environment - Part 1: Getting Started with VIM"
date: 2022-05-13
showToc: false
TocOpen: false
hidemeta: false
comments: false
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowRssButtonInSectionTermList: true
tags: [Tutorial, Vim]
---

![](https://imgs.xkcd.com/comics/hottest_editors.png#center)
*Source: xkcd Comic*

# Introduction

Current or aspiring Engineer/Scientist are very likely to end up in a situation where coding will be required. I coded nearly every day in my jobs so far and it is therefore worthwhile to spend some time on finding and configuring available tools to ensure a smooth and productive experience.

My goal for this series is to describe how to set up a functioning coding environment on MacOS (Linux distros will be very similar if not the same). I will go through the tools that I have used in the past, but there are a plethora of tools out there. Feel free to explore and try out other ones for yourself as the choice sometimes falls down to simple personal preference.

# Choosing an Editor

Generally speaking, code can be edited using different software/programs. Some come built-in in the Operating System (OS), others need to be installed separately. These software can be divided into the following categories:

- Text Editors: As the name suggests, they are primarily used to edit text. As such, they tend to be lightweight and do not come with a great number of features. Features can however be added via Plugins. Notable examples are _VIM_ and _emacs_. 
- IDEs: Integrated Development Environments are full fledged software which contain a considerable amount of features specifically designed to help develop and test code. Some IDEs are language specific, such as PyCharm or Spyder for Python. Another example is the widely used Visual Studio Code (VSC) program from Microsoft.

So which one should we choose? That will strongly depend on the tasks/needs. In case of local software development, having an IDE can be the way to go since it will help us to quickly develop and test our code. On the other hand, Text Editors are the go-to option when working with remote servers. A personal anecdote is that my code was running at least one order of magnitude faster when executed from the command line rather from the Spyder environment.

It is probably best to have good working knowledge of at least one tool in each above category just to cover all possible needs. Personally, I use Spyder for quick prototyping but extensively use VIM when developing and testing code.

VIM is an awesome tool that does have a somewhat steep initial learning curve and therefore requires some time to get the hang out of it. However, the productivity boost obtained when used appropriately is amazing. That is due to the philosophy of VIM which discourages the use of the mouse and arrow keys. The goal is to code at the speed of thought with minimal number of keystrokes.

# Getting started with VIM

It is very likely that VIM is already installed. This can be checked It is very likely that VIM is already installed. This can be checked by typing into the command line:
```
vim
```
and can be quit with the command `:q` inside the editor.

In case that VIM is not installed or found, it can be installed by following the instructions at [https://www.tutorialspoint.com/vim/vim_installation_and_configuration.htm](https://www.tutorialspoint.com/vim/vim_installation_and_configuration.htm).
J
## Getting around VIM

Typing `vimtutor` in the command line will, you guessed it, bring up the tutorial program for vim. It is a great resource to get started and learn the basic commands and how to navigate. It should only requires one or two hours to complete. It is also pretty exhaustive on the basics, so definitely worth checking out. 

As for the rest: Google or any other search engine is our friend! I have always found my way around VIM by googling around my questions and I learned a lot by looking at other peoples configuration file which we will discuss in the next post.

# Summary

We now have basic knowledge about the VIM text editor and can start editing files on our local computer or even remote servers! VIM shines through its philosophy which encourages enhancing productivity as well as the fact that it is usually available on most systems from the get-go.

Vanilla VIM is not very powerful or impressive when it comes to code development. In the next post, we will see how we can configure and add plugins to drastically increase VIMs capabilities.
