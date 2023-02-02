---
layout: post
title:  "Fab Lab 3D Printing: Prusa Slicer Setup and Use (CLI for Screen Readers)"
date:   1113-01-01
last_modified_at: 2023-01-26
categories: [Fabrication Lab]
tags: [3D Printing]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

## Learning Objectives
In this lesson you will learn how to set up and use the Prusa Slicer software (CLI) with the command line shell. As the graphical user interface for Prusa Slicer is not fully accessible using the command line shell you can access all of the different slicer features through a hand text interface. After you have sliced your model we will briefly go through steps on how to print it using a Prusa Mk3S printer.
<br><br><br>

## Pre-Requisites 
- basic command line knowledge
- typing skills
- basic knowledge of how command lines work and folder and file navigation
<br><br><br>

## Prusa Slicer Install (Windows)
[Download Prusa Slicer if you have not already.](https://www.prusa3d.com/page/prusaslicer_424/)
<br><br>

1. Alt + n for next page from intro page
2. Choose installation type we recommend installing for everyboday (default). Alt + n for next page.
3. Choose where to install the program files we recommend the default location, if you choose another location make sure you make note because you will need the path to the CLI .exe file if you want to add the CLI to your PATH environment variable. Alt + n for next page.
4. Select the features. Tab and you will be in the tree view of check boxes to select. Here you will select your drivers and different utilities that are included with the slicer. We recommend adding the driver for your Prusa printer if you have one, if not the defaults will work. Alt + n for next page.
5. Create application shortcuts. Go with the defaults to have a shortcut added to your start menu and desktop. Alt + i to install
6. You may prompted with a "user account control" dialogue you will need to input an administrator user name and password and then a security dialogue will pop up asking if you want to install tab to the install button when the security dialogue is focused or type alt + i.
7. You should be notified that the installation was successful. Alt + f to finish.
<br><br>

### CLI Windows Install
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
[In this folder](https://github.com/funkonaut/openSCAD_lessons/tree/main/3D_Printing/profiles) you will find different slicing profiles for different printers. We obtained these by setting up the profile in the prusa-slicer GUI program (not very accessible) and exporting them to .ini files you can use these with your printer. Feel free to contribute ini files for other printers. Using a profile can be helpful to get you started printing fast. You can download these via git or open the .ini file and tab to the "raw" button select all and copy it into an empty .ini file on your computer. 
<br><br>

*Note if you try to download a configuration profile and you hear a warning about the file harming your computer hit f6 until you move to the downloads bar and tab to "keep".*
<br><br>

### Steps for Basic Printing 
1. Determine the model of printer you are using and type of material you are printing in and download a configuration profile for the printer, make sure it is either in the same directory that you are located in or you know the path to it. *Note: It is possible to not use a configuration profile and use several command line flags but we recommend for beginners to use a profile that best suites their needs and then modify them as needed by editing the configuration file or overriding the file with command line flags*
2. Run the following command, where you replace the paths in brackets with the configuration file and model file paths: `prusa-slicer-console.exe -g --load [./my_config.ini] [./my_model.stl]` You should receive output stating the file is done slicing, it will be available in your current directory as where layer-height, material, and supports/no-supports are determined by your configuration file probably something like: `[filename]_[layer-height]_[material]_[printer-model]_[time-to-print].gcode`
3. Plug in your 3D printer SD card to your computer and determine the drive name of your external media (3D printer SD card) use the list drives command or guess and see if powershell throws an error (ie `ls d:` `ls e:` `ls f:` etc.)
4. Move your file to your external media. We recommend starting with a fresh SD card and having your file in the root directory that way step five is easier. `mv [path_to_sliced_file.gcode] [path_to_drive]`
5. Put SD card back into the printer slot listen for the beep it will default you to the SD card menu turn the wheel one click and then press it, it should start printing the file you most recently uploaded as long as it is in the root directory of the external drive (3D printer SD card).  
<br><br>

### Troubleshooting
- Sometimes if your command is incorrect you will launch the Prusa Slicer GUI
- If your slicer fails to slice try making sure you are in the same folder as your .stl file
- Determine that the model size fits on your print bed (max for MK3s is 250 by 210 by 210). Run: `prusa-slicer-console.exe --info [./my_model.stl]]`
<br><br><br>

## Adding or Creating a New Config File in the GUI
- Launch the Prusa Slicer GUI application and run the configuration wizard to download different printer and filament profiles.
- Set up the configuration you'd like to export.
- Export config from prusa slicer GUI (file > export config or ctrl + e) and name it as `[layer-height]_[material]_[printer-name]_[supports/no-supports]`
<br><br><br>

## Review
In this lesson you learned:
- How to set up Prusa Slicer CLI
- How to use the Prusa Slicer CLI with a configuration profile to slice a 3D model
- How to print using an SD card with the Prusa MK3s printer
<br><br><br>

## Resources
- [Download Prusa Slicer](https://www.prusa3d.com/page/prusaslicer_424/)
- [3D printing configuration profiles repo for Prusa Slicer](https://github.com/funkonaut/openSCAD_lessons/tree/main/3D_Printing/profiles)
<br><br><br>




