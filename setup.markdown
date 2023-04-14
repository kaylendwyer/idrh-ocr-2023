---
layout: page
title: Setup
permalink: /setup/
nav_order: 2
---

# Setting things up

Attendees do not need to install anything to their own systems.

However, if you are not from KU, you will need one of the following:

* Shibboleth
* InCommon institutional login
* GitHub account
* ORCID account

This workshop uses an image in Jupyter Hub, allowing each student to run tesseract in the command line without installation. Our goal is to offer an introduction to OCR and Tesseract without additional tools mediating or confusing that process.


## Working from home
### Install software
If you do not already have the shell software installed, you will need to [download and install it](https://carpentries.github.io/workshop-template/#shell).

### Open a new shell
After installing the software
1. Open a terminal. If you're not sure how to open a terminal on your operating system, see the instructions below.
2. In the terminal type ```cd``` then press the **Return** key. This step will make sure you start with your home folder as your working directory.

### Where to type commands ####
**Windows**

Computers with Windows operating systems do not automatically have a Unix Shell program installed. In this lesson, we encourage you to use an emulator included in [Git for Windows](https://carpentries.github.io/workshop-template/#shell), which gives you access to both Bash shell commands and Git.

Once installed, you can open a terminal by running the program Git Bash from the Windows start menu.

**macOS**

For a Mac computer running macOS Mojave or earlier releases, the default Unix Shell is Bash. For a Mac computer running macOS Catalina or later releases, the default Unix Shell is Zsh. Your default shell is available via the Terminal program within your Utilities folder.

To open Terminal, try one or both of the following:

* In Finder, select the Go menu, then select Utilities. Locate Terminal in the Utilities folder and open it.
* Use the Mac ‘Spotlight’ computer search function. Search for: ```Terminal``` and press **Return.**
To check if your machine is set up to use something other than Bash, type ```echo $SHELL``` in your terminal window.

If your machine is set up to use something other than Bash, you can run it by opening a terminal and typing ```bash```.

Read: [How to Use Terminal on a Mac](http://www.macworld.co.uk/feature/mac-software/how-use-terminal-on-mac-3608274/)


### Installing Tesseract
If you would like to use tesseract on your own machine, follow the [installation guidelines in the tesseract documentation.](https://tesseract-ocr.github.io/tessdoc/#compiling-and-installation)


If you do not have administrator rights to your computer, you will need to configure Tesseract specially to use it.


The OCR lessons use images in a [zipped file on the GitHub repository](https://github.com/kaylendwyer/idrh-ocr-2023/blob/main/OCR-images.zip).

