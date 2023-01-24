---
layout: post
title:  "3D Printing Slicing/Printing: Prusa Slicer Setup and Use"
date:   1113-01-01
last_modified_at: 2023-01-24
categories: [3D Printing]
tags: [Slicing/Printing]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

## Learning Objectives
In this lesson you will learn how to set up and use the Prusa Slicer software with the command line shell. As the graphical user interface for Prusa Slicer is not fully accessible using the command line shell you can access all of the different slicer features through a hand text interface. After you have sliced your model we will briefly go through steps on how to print it using a Prusa Mk3S printer. In the next article we will go through how to print using [the octoprint server](https://octoprint.org/) a web interface for your 3D printer that will be more easily extendable to other 3D printers with an octoprint server set up.
<br><br><br>

## Pre-Requisites 
- basic command line knowledge
- typing skills
- basic knowledge of how command lines work and folder nav file navigation
<br><br><br>

## Command Line Prusa Slicer Install
- [Download Prusa Slicer](https://www.prusa3d.com/page/prusaslicer_424/)
<br><br>

### Windows Install
These steps will allow you to run the Prusa Slicer program from anywhere and not just in the program folder. You will add the prusa-slicer-console.exe to your system environment variables PATH variable, so you do not have to type the whole path to the Prusa Slicer CLI every time you want to run the slicer from the command line.  
<br><br>

1. Open powershell (as admin) (Windows + X > a)
  - *Note: Sometimes Windows will prompt you with an inaccessible system dialog, if you are not hearing your powershell open try changing focus to "User Account Control" hitting tab twice and then pressing enter, you may be prompted for a user name and password if your account does not have admin credentials*
2. Type `[Environment]::SetEnvironmentVariable("Path", $env:Path + ";C:\Program Files\Prusa3D\PrusaSlicer", "Machine")` replace `C:\Program Files\Prusa3D\PrusaSlicer` with whatever the path to your slic3r program folder is
3. *If you do not have admin access* You can check out [this article about customizing your shell profile](https://www.howtogeek.com/50236/customizing-your-powershell-profile/) and [this stack overflow answer](https://stackoverflow.com/questions/714877/setting-windows-powershell-environment-variables) but we recommend trying to get admin access to your system.
4. Test and make sure it worked by running powershell and typing `pru` and pressing tab a couple times it should autocomplete to `prusa-slicer-console.exe` after two tabs and then add the help flag the whole command should read `prusa-slicer-console.exe --help` and will output a whole lot of text you can output it to a text file (ie: `prusa-slicer-console.exe --help > prusa-slicer_help.txt` if you are interested in reading it or [visit the slic3r documentation page on using the command line tools](https://manual.slic3r.org/advanced/command-line)
<br><br>

*Note: The prusa-slicer-console exe is the one you want for command line commands the other slicer exe files are not for command line usage, and will most likely launch the less than accessible GUI program*
<br><br><br>

## Using Prusa Slicer CLI
In this folder you will find a subfolder [profiles](https://github.com/funkonaut/openSCAD_lessons/tree/main/3D_Printing/profiles) that will have different slicing profiles for different printers. We obtained these by setting up the profile in the prusa-slicer GUI program (not very accessible) and exporting them to .ini files you can use these with your printer. Feel free to contribute ini files for other printers. Using a profile can be helpful to get you started printing fast.
<br><br>

*Note if you try to download a configuration profile and it is not showing up in your Downloads folder you may be getting a warning from your browser press f6 to switch to the browser pane with the warning and tab to "keep" and press enter.*
<br><br>

### Steps for Basic Printing 
1. Determine the model of printer you are using and type of material you are printing in and download a configuration profile for the printer, make sure it is either in the same directory that you are located in or you know the path to it. *Note: It is possible to not use a configuration profile and use several command line flags but we recommend for beginners to use a profile that best suites their needs and then modify them as needed by editing the configuration file or overriding the file with command line flags*
2. Run the following command, where you replace the paths in brackets with the configuration file and model file paths: `prusa-slicer-console.exe -g --load [./my_config.ini] [./my_model.stl]` You should receive output stating the file is done slicing, it will be available in your current directory as where layer-height, material, and supports/no-supports are determined by your configuration file probably something like: `[filename]_[layer-height]_[material]_[printer-model]_[time-to-print].gcode`
3. Plug in your 3D printer SD card to your computer and determine the drive name of your external media (3D printer SD card) use the list drives command or guess and see if powershell throws an error (ie `ls d:` `ls e:` `ls f:` etc.)
4. Move your file to your external media. We recommend starting with a fresh SD card and having your file in the root directory that way step five is easier.
5. Put SD card back into the printer slot listen for the beep it will default you to the SD card menu turn the wheel one click and then press it, it should start printing the file you most recently uploaded as long as it is in the root directory of the external drive (3D printer SD card).  
<br><br>

### Troubleshooting
- Sometimes if your command is incorrect you will launch the Prusa Slicer GUI
- Determine that the model size fits on your print bed (max for MK3s is 250 by 210 by 210). Run: `prusa-slicer-console.exe --info [./my_model.stl]]`
<br><br><br>

## Adding or Creating a New Config File in the GUI
- Set your slicer config (probably best to keep infill default at 20% and just use command line flags to override it)
- Export config from prusa slicer GUI (file > export config or ctrl + e) and name it as `[layer-height]_[material]_[printer-name]_[supports/no-supports]`
<br><br><br>

## Review
In this lesson you learned:
- How to set up Prusa Slicer CLI
- How to use the prusa slicer CLI with a configuration profile to slice a 3D model
- How to print using an SD card with the Prusa MK3s printer
<br><br><br>

## Resources
- [Download Prusa Slicer](https://www.prusa3d.com/page/prusaslicer_424/)
- [3D printing configuration profiles for Prusa Slicer](https://github.com/funkonaut/openSCAD_lessons/tree/main/3D_Printing/profiles)
<br><br><br>




