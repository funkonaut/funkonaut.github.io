---
layout: post
title:  "Advanced File and Folder Operations"
date:   1114-01-01
last_modified_at: 2024-1-25
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
- Basic knowledge of what a computer **operating system** is and its features (ie file/folders/applications/shortcuts/file extentions/etc.)
- Basic knowledge of computer hardware (hard drive/usb and other peripheral ports/cloud vs local storage)
- Basic understanding of variables and parameters
- Basic internet navigation skills and (URL structure)
- Getting started Lesson for [Power Shell](https://www.accessiblestem.org/command%20line%20shell/cls-1.html) 
- Command Line Shell Intro: Copying, Moving, Creating and Removing Files and Folders [Lesson 2](https://www.accessiblestem.org/command%20line%20shell/cls-copy-move.html)
<br><br><br>

## Lesson Overview
In this lesson we will cover some more advanced file and folder operations, as well as talk about outputting text the power shell window, redirecting powershell output to different files, launching programs from the power shell. We will also discuss piping (or chaining multiple) commands and see more of the power of learning the power shell! By the end of this lesson you will be able to create and edit text files in the powershell and in the notepad.exe application, launch a file explorer window (the graphical way one typically accesses files and folders on your computer) or a default application from a directory or for a file, and how to chain multiple commands in one entry prompt to make your computer access even more efficient! 
<br><br><br>

## The Echo Command
The echo command will parrot, or rather echo what ever you type as an argument. It will output each argument on a new line that follows your command prompt. For example type the command `echo "hello world"` this will output the phrase hello world to the powershell. You typically want to type your argument surrounded by quotes. When an argument is surrounded by quotes it is known as a **string**. If you do not include quotes in your argument then powershell will output two lines for each word. This is because powershell is interpreting each word as a separate argument. Just like with paths with spaces in it as powershell separates arguments with spaces you must include quotes around arguments with spaces if you want powershell to interpret it as one argument, as in outputting it as one line and not multiple.
<br><br>

We will see soon why the echo command is useful. As well when you learn how to write code using the command line shell (also known as bash scripting) the echo command is useful for directing or displaying information to your user.
<br><br><br>

## The Redirect Symbol >
By default information that is outputted from commands is output directly to the powershell, but there a re a plenty of cases when you want to redirect the output of a command to a file or another place on your computer. For instance if your command outputs a lot of information and you want to save it you can redirect the commands output using the redirect symbol to a file. In order to do this for instance to save the list of files in a folder you could type:
`ls ./ > files_here.txt` 
<br><br>

Nothing would appear in the powershell after you entered this command, but there would now be a file named "files_here.txt" in your present (current) working directory that has what would have been outputted to the powershell.  
<br><br><br>

### Creating New Files with the Redirect Symbol
- std err?

<br><br><br>

## The Append Operator >>
<br><br><br>

## Launching Programs
<br><br>

### Launching Notepad from the Powershell
<br><br>

### Launching the File Explorer from the Powershell
<br><br>

#### A note on default applications...
<br><br><br>

## The Pipe Symbol
<br><br><br>

## Checks for Understanding
1. 
<br><br><br>

## NEXT STEPS
- clear
- history
- man
- processes ps
- kill
- control + c, control + z 
- extracting files and folder 
- environment variables
- ssh
- wget
<br><br>

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
- [Moving files linux tutorial](https://ioflood.com/blog/mv-linux-command/)
- [Another move linux tutorial](https://linuxize.com/post/how-to-move-files-in-linux-with-mv-command/)