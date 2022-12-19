---
layout: post
title:  "Prusa Slicer: Your First 3D Print"
date:   2333-01-01
last_modified_at: 2022-12-18
categories: [3D Printing]
tags: [Slicing]
---

## Pre-Requisites 
- basic command line knowledge
- typing skills
- basic knowledge of how command lines work and folder nav file navigation

# Getting Started with Prusa Slicer CLI

## Pre-Requisites 
- basic command line knowledge
- typing skills
- basic knowledge of how command lines work and folder nav file navigation

## Command Line Prusa Slicer Install
- [Download Prusa Slicer](https://www.prusa3d.com/page/prusaslicer_424/)

### Windows Install
These steps will allow you to run the Prusa-Slicer program from anywhere and not just in the program folder. You will add the prusa-slicer-console.exe to your system environment variables PATH variable 
1. Open powershell (as admin)
2. *If you do have admin access* Run powershell as admin and type `[Environment]::SetEnvironmentVariable("Path", $env:Path + ";C:\Program Files\Prusa3D\PrusaSlicer", "Machine")` replace `C:\Program Files\Prusa3D\PrusaSlicer` with whatever the path to your slic3r program folder is
3. *If you do not have admin access* You can check out [this article about customizing your shell profile](https://www.howtogeek.com/50236/customizing-your-powershell-profile/) and [this stack overflow answer](https://stackoverflow.com/questions/714877/setting-windows-powershell-environment-variables)
4. Test and make sure it worked by running powershell and typing `pru` and pressing tab a couple times it should autocomplete to `prusa-slicer-console.exe` and then add the help flag the whole command should read `prusa-slicer-console.exe --help` and will output a whole lot of text you can output it to a text file (ie: `prusa-slicer-console.exe --help > prusa-slicer_help.txt` if you are interested in reading it or [visit the slic3r documentation page on using the command line tools](https://manual.slic3r.org/advanced/command-line)
*Note:The prusa-slicer-console exe is the one you want for command line commands the other slicer exe files are not for command line usage, and will most likely launch the less than accessible GUI program*

## Using Prusa Slicer CLI
**We highly recommend [reading the docs for Slic3r which is what prusa-slicer is based around!](https://manual.slic3r.org/advanced/command-line), thats why we have linked them twice already in this documentation!**
In this folder you will find a subfolder [profiles](../../3D_Printing/profiles) that will have different slicing profiles for different printers. We obtained these by setting up the profile in the prusa-slicer GUI program (not very accessible) and exporting them to .ini files you can use these with your printer. Feel free to contribute ini files for other printers. Using a profile can be helpful to get you started printing fast.

**MAYBE MAKE NOTE OF CONFIG FILES DEFAULT INFILL SETTING...**

### Steps for basic printing 
1. Determine the model of printer you are using and type of material you are printing in and download a configuration profile for the printer, make sure it is either in the same directory that you are located in or you know the path to it. *Note: It is possible to not use a configuration profile and use several command line flags but we recommend for beginners to use a profile that best suites their needs and then modify them as needed by editing the configuration file or overriding the file with command line flags*
2. Run the following command, where you replace the paths in brackets with the configuration file and model file paths:
 `prusa-slicer-console.exe -g --load [./my_config.ini] [./my_model.stl]`
You should recieve output stating the file is done slicing, it will be availble in your current directory as where layer-height, material, and supports/no-supports are determined by your configuration file:
`[filename]_[layer-height]_[material]_[printer-model]_[time-to-print].gcode`
3. Determine drive name of your external media (3D printer SD card) use command or guess and tab complete...
4. Move file to your external media 
5. Put drive back into printer listen for the beep it will default you to the sd card menu turn the wheel one click and then press it, it should start printing the file you just uploaded as long as it is in the root directory of the external drive (3D printer SD card).  

### Troubleshooting
- Determine that the model size fits on your print bed (max for MK3s is 250 by 210 by 210). Run: `prusa-slicer-console.exe --info [./my_model.stl]]`


## Adding or creating a new config file
- Set your slicer config (probably best to keep infill default at 20% and just use command line flags to override it)
- Export config from prusa slicer GUI (file > export config or ctrl + e) and name it as `[layer-height]_[material]_[printer-name]_[supports/no-supports]`


