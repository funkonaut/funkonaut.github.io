---
layout: post
title:  "Command Line Shell Intro: Getting Started on the Right Path"
date:   1114-01-01
last_modified_at: 2024-1-11
categories: [Command Line Shell]
tags: [Intro]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

## Pre-Requisite Knowledge
- Typing skills
- Text editing skills
- Basic Windows Navigation skills
- Basic screen reading skills
- Basic knowledge of what a computer **operating system** is and its features (ie file/folders/applications/shortcuts/file extenstions/etc.)
- Basic knowledge of computer hardware (hard drive/usb and other peripheral ports/cloud vs local storage)
- Basic understanding of variables and parameters
- Basic internet navigation skills and (URL structure)
- Getting started Lesson for [Power Shell](https://www.accessiblestem.org/command%20line%20shell/cls-1.html) 
<br><br><br>

## Lesson Overview
Now that you under stand some basic navigational concepts in the powershell we will now cover the basics of data manipulation using powershell commands, namely making folders, moving files and folders, renaming files and folders, copying files and folders, and deleting files and folders.

### Copying, Moving, Creating, and Removing Files and Folders
Use commands like `mv`, `cp`, `mkdir`, `rm`, and `rmdir` to manipulate files and folders. Be cautious when using these commands, as they can delete data permanently. For instance try out the following:
<br><br>

Let's start in the user's home directory and change into the "Documents" folder.
`cd ~` 
`cd Documents`
<br><br>

To create a new directory use the `mkdir` command it stands for make directory. This command takes an argument of a folder name or a path to a folder name. Now that you are in your documents you can make a directory called "SampleFolder"
mkdir SampleFolder

# List the contents of "SampleFolder" it will be empty
ls .\SampleFolder

# Copy a file from downloads

# Move "File1.txt" to a new location "SampleFolder\SubFolder1"
mv .\SampleFolder\File1.txt .\SampleFolder\SubFolder1\File1.txt

# Copy "File2.txt" to a new location "SampleFolder\SubFolder2"
cp .\SampleFolder\File2.txt .\SampleFolder\SubFolder2\File2.txt

# List the contents of "SampleFolder" to see the changes after moving and copying
ls .\SampleFolder

# Remove "File1.txt" from "SampleFolder"
rm .\SampleFolder\SubFolder1\File1.txt

# Remove "SubFolder1" from "SampleFolder"
rmdir .\SampleFolder\SubFolder1

# List the contents of "SampleFolder" after the removal
ls .\SampleFolder
```

### Autocompletion and Wildcards
As we learning in the getting started lesson power shell supporting autocompletion using the tab key. Pressing tab will cycle through the files in the directory you are located in based upon what you type. It will also add quotes around paths to files that have spaces. You can also use wildcards like `*` (matching zero or more characters) and `?` (matching a single character) for pattern-based searching. So for

EXAMPLES

## Additional Resources
For more in-depth learning and advanced usage of PowerShell, consider exploring the following helpful resources:

- [Accessibility in PowerShell ISE by Microsoft](https://learn.microsoft.com/en-us/powershell/scripting/windows-powershell/ise/accessibility-in-windows-powershell-ise?view=powershell-7.3)
- [Learn PowerShell by Microsoft](https://learn.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7.3)
- [Setting the PATH Variable in PowerShell](https://poshcode.gitbook.io/powershell-faq/src/getting-started/environment-variables)
- [PowerShell Aliases](https://learn.microsoft.com/en-us/powershell/scripting/learn/shell/using-aliases?view=powershell-7.3)
- [Linux Commands Cheat Sheet](https://www.guru99.com/linux-commands-cheat-sheet.html)
- [PowerShell Cheat Sheet](https://www.theochem.ru.nl/~pwormer/teachmat/PS_cheat_sheet.html)
- [Learn PowerShell on GitHub](https://github.com/PowerShell/PowerShell/tree/master/docs/learning-powershell)
- [PowerShell Tutorial on Guru99](https://www.guru99.com/powershell-tutorial.html)