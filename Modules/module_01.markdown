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

---

## Working with files and directories

### Moving into and creating new directories

We will work with files located in our `shell-lesson` directory:
- `cd shell-lesson`

To make a new directory:
- `mkdir firstdir`

When working in the shell, it's important to use **no spaces** in file and directory names. The space character tells the shell to look for the next command or input. Spaces in file and directory names will cause you trouble.

### Exploring files

We can use several methods to find out the contents of a file.

`cat` stands for "concatenate" and reads the contents of a file out onto the screen:
- `cat 829-0.txt`
- For long files such as this one, it's too much information at once

Instead, we can peek at the first or last 10 lines of a file:
- `head 829-0.txt` displays the first 10 lines of the file on the screen
- `tail 829-0.txt` displays the last 10 lines of the file on the screen

Or, to see more information in a controlled way, we can put the file into a reader called the `pager` using the command `less`:
- `less 829-0.txt`

Inside the `pager` we can move page by page:
- `spacebar` moves forward
- `b` moves backward
- `q` to quit the pager

### Wildcards

The shell has two commonly-used wildcard characters:
- `*` stands for "zero or more characters"
- `?` stands for "one character"

Wildcards help us work with multiple files at once and save typing.

Instead of `head 829-0.txt 33504-0.txt` to see the first 10 lines of two files, we can use a wildcard: `head *.txt`

### Redirect and Append

To get only the first line of a file, we can tweak the `head` command:
- `head -n 1 829-0.txt 33504-0.txt`

Instead of getting these two lines on the screen, we can redirect them to a file using `>`:
- `head -n 1 829-0.txt 33504-0.txt > book-titles.txt`

`>` will erase the existing contents of a file. If we need to add information from another file to `book-titles.txt` without erasing our work, we can append to the bottom of the file using `>>`:
- `head -n 1 pg514.txt >> book-titles.txt`

### Copy, Move, and Delete

Let's back up our files using the `backup/` directory. We make a copy of each file, giving it a clearer file name, then move it into `backup/`:
- `cp 829-0.txt gulliver.txt`
- `mv gulliver.txt backup`

We can combine this into one command by telling `cp` to put the copied file in the `backup/` directory:
- `cp 33504-0.txt backup/opticks.txt`

`mv` and `cp` will overwrite any existing file that has the same name as the file being moved or copied. Be careful to avoid data loss.

To clean up our workspace, we can delete files and directories we don't need:
- `rm book-titles.txt` means "remove" the file
- `rmdir firstdir` means "remove a directory

`rm` and `rmdir` are permanent and forever in the shell. There is no recycle bin or trash can to save you. Be careful what and when you delete.
