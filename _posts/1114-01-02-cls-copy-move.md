---
layout: post
title:  "Command Line Shell Intro: Copying, Moving, Creating and Removing Files and Folders"
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

#### Making Directories
Let's start in the user's home directory and change into the "Documents" folder.
`cd ~` 
`cd Documents`
<br><br>

To create a new directory use the `mkdir` command it stands for make directory. This command takes an argument of a folder name or a path to a folder name. Now that you are in your documents you can make a directory called "sample_folder"
`mkdir sample_folder`
<br><br>

When you create a directory the contents of the directory will be empty type:
`ls .\sample_folder`
<br><br>

##### Quick Quiz!
Can you navigate into the sample folder and list the files and subfolders (there should be none) inside it?
<br><br>

You can also give the `mkdir` command a path. For instance change back to your home directory and then make a directory in your documents folder called another_folder that way you don't have to change into your documents directory saves you a command. Remember you can do auto complete by hitting tab when typing in paths, type the first few letters of the path for instance `~/doc` and hit tab and let the computer do the work for you! 
`cd ~/`
`mkdir ~/Document/another_folder`
<br><br>

*Also notice you can do `cd ~/` or `cd ~` the slash separates sub-directories or files in your path and if there is nothing following it the computer will just ignore it.*
<br><br>

#### Copying Files and Directories
To copy a directory we use the `cp` command, which stands for... you guessed it copy! `cp` takes an argument of two paths. First comes the path of the file(s) or folder(s) you want to copy, ie the **source** or sources and then the path of where you want to copy it to, ie the **destination**. 
<br><br>

##### Copy a file from downloads
If you have a file in downloads you can use it or you can []<a href="{{ site.url }}/downloads/blank_file.txt" download>click here to download this blank_file.txt file</a> and Windows should put it in your downloads folder.
<br><br>

1. Copy blank file from your downloads to your documents using absolute paths
`cp ~/Downloads/blank_file.txt ~/Documents`
2. Copy blank file from your downloads to your another_folder in the documents folders using a relative path for the source and an absolute path for the destination
`cd ~/Downloads`
`cp ./blank_file.txt ~/Documents/another_folder`
3. Check and make sure it copied using the list command with a relative path!
`cd ~/Documents/another_folder`
`ls -n .` you could also type `ls -n` powershell will default to thinking you mean the current directory if you do not type a path.
<br><br>

##### Copy a directory using the -r option
You can copy a folder similarly to how you copy a file, however you will need to include the -r option, also known as the -r **flag**, or the **recurse** flag. The recurse flag will copy the directory and all the files and folders that may be in the directory too. You can not copy just a directory but not the files and folders in the directory, you have to copy it all! Not using the -r flag may work, but it is good practice to use it as other shells like Linux and Mac OS terminal require it.
<br><br>

1. Copy your another_folder into your Downloads using absolute paths.
`cp -r ~/Documents/another_folder ~/Downloads`
2. Copy your sample_folder from your Documents into your Downloads folder using relative paths.
`cd ~/Documents`
`cp -r ./sample_folder ~/Downloads`
<br><br>

###### Copying multiple files and folders
You can use the copy command to copy multiple files and folders. The way the command is structured is the same you can separate multiple source paths with spaces. For instance to copy another_folder and the blank_file.txt to the sample_folder in your documents enter the command:
`cp ~/Documents/another_folder ~/Downloads/blank_file.txt ~/Documents/sample_folder`
<br><br>

##### Moving files and folders
You can use the `mv` command to move files and folders. The move takes a source (or sources) path to the files and folders you want to move and also takes a destination path, ie where you want to move them to. The `mv` command will overwrite any files in the destination that are named the same as the source file and you can not recover this data if you accidentally overwrote an important file. The `mv` command can also  be risky as unlike the `cp` the `mv` command does not copy the original file it moves it. Just like copy move can take multiple source paths if you want to move multiple files or folders at once. Unlike copy the `mv` command does not require the recurse flag, -r, to work with folders! 
<br><br>

1. Move the file blank_file.txt from your Downloads into your sample_folder in your Documents. There will no longer be a blank_file.txt in your Downloads you can list the files in your Downloads directory to confirm as it is now in your Documents/sample_folder. This move command will also overwrite the file you copied previously into sample_folder as they are the same you won't really notice anything changed.
`mv ~/Downloads/blank_file.txt ~/Documents/sample_folder`
`ls -n ~/Downloads`
`ls -n ~/Documents/sample_folder`
2. List the contents of the subfolder sample_folder in your Documents. You should have a subfolder another_folder and the blank_file.txt in it.
`ls -n ~/Documents/sample_folder`
3. Move the copied sample_folder and the copied another_folder from your downloads to your Documents. Notice that as we already have a sample_folder and another_folder in our documents these got over written. If your sample_folder in your downloads had nothing in it then you should have an empty sample_folder in your Documents now.
`mv ~/Downloads/sample_folder ~/Downloads/another_folder ~/Documents`
`ls -n ~/Documents/sample_folder`
<br><br>

###### Renaming files and folders with mv and copy
In order to rename files and folders using the powershell you can use the move command. It works the same way except you can just use the current directory as the destination path and include the new file name as part of the path, if you do not include a new file name it will default to just moving it to the path you specified.
1. Rename blank_file.txt in  Documents/sample_folder to empty_file.txt
Using relative paths:
`cd ~/Documents/sample_folder`
`mv ./blank_file.txt ./empty_file.txt`
Using absolute paths:
`mv ~/Documents/sample_folder/blank_file.txt ~/Documents/sample_folder/empty_file.txt`

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