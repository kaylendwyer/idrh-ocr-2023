---
layout: page
title: Unix Shell
permalink: /unix-shell/
nav_order: 1
parent: Modules
---

# Introduction to the Shell

## What is the shell?

- A program that allows you to interact with your computer using typed text commands
- Commands respond by generating output
- Output can come to the screen, or can be directed to a file or other commands
- Chaining commands together makes it possible to automate a series of actions

This session introduces:
- Basic commands to interact with the file system
- Manipulating files and their contents
- Working with many files at once

---

## Navigating in the shell

### The Prompt

We type commands at the shell's prompt, which looks like `$`. Sometimes the prompt includes additional information.

### The File System

The file system is the part of the operating system that manages files and directories (folders):
- Files: hold information
- Directories: hold files, other directories, or both

The file system is hierarchical, so think about smaller containers nested inside bigger containers.

### Moving around in the File System

Three key commands answer some important questions:
- `pwd` stands for "print working directory" and means "Where am I?"
- `ls` stands for "list" and means "What is here with me?"
- `cd` stands for "change directory" and means "Get me out of here!"

Commands often take additional information, called arguments, to make their actions more specific.

`ls` takes many possible arguments to change how the contents of a directory are displayed. Common `ls` arguments are:
- `ls -l`: "list long" to show more information about the contents of a directory
- `ls -lh`: "list long human" to include human-readable file size information

We can find out more about any command by invoking the manual for that command:
- `man ls` is a good way to find out what arguments `ls` can take

To move to a different directory, we tell the `cd` command where we want to go within the current working directory:
- `cd shell-lesson`

An important shortcut allows us to move into the parent directory of our current working directory, in effect backing out of our file system:
- `cd ..`
