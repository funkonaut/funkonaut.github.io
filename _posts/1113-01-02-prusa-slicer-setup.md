---
layout: post
title:  "Fab Lab 3D Printing: Prusa Slicer Setup"
date:   1113-01-02
last_modified_at: 2023-06-16
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
In this lesson you will learn how to set up the Prusa Slicer software. The graphical user interface for Prusa Slicer is not fully accessible but has several keyboard shortcuts and features that  enables efficient low vision access and limited screen reader access. 
<br><br><br>

## Pre-Requisites 
- basic Windows navigation
- basic folder and file navigation in Windows
<br><br><br>

## Prusa Slicer Install (Windows)
[Download Prusa Slicer if you have not already.](https://www.prusa3d.com/page/prusaslicer_424/)
<br><br>

1. Alt + n for next page from intro page
2. Choose installation type we recommend installing for everybody (default). Alt + n for next page.
3. Choose where to install the program files we recommend the default location. Alt + n for next page.
4. Select the features. Tab and you will be in the tree view of check boxes to select. Here you will select your drivers and different utilities that are included with the slicer. We recommend adding the driver for your Prusa printer if you have one, if not the defaults will work. Alt + n for next page.
5. Create application shortcuts. Go with the defaults to have a shortcut added to your start menu and desktop. Alt + i to install
6. You may prompted with a "user account control" dialogue you will need to input an administrator user name and password and then a security dialogue will pop up asking if you want to install tab to the install button when the security dialogue is focused or type alt + i.
7. You should be notified that the installation was successful. Alt + f to finish.
<br><br>

### Running Prusa Slicer the First Time
When you first run Prusa Slicer the configuration wizard will run. Here we will configure our slicer GUI and will download configuration profiles for different printers and materials. We recommend sticking to only a couple profiles to not overwhelm you with options. You can always relaunch the configuration wizard in the help menu (alt > c > w). 
<br><br>

1. Alt + N to move past the welcome menu
2. Prusa FFF: Select your FFF Prusa 3D printer if you have one and nozzle size (.4mm is the default) 
3. Prusa MSLA: Select your MSLA Prusa printer (odds are you probably don't have one of these, it is also known as a resin printer)
4. Other Vendors: If you have another vender (Creality is a popular one...) you can select it from the check list and it will prompt you for the printer in the next window (alt + n)
5. Custom Printer: You can define a custom printer profile you probably just want to skip this...
6. Filaments: Now we will add filament profiles. We recommend starting with the "Generic PLA" Profile option (make sure to click None first to uncheck the default options). If you know the brand of filament that you have purchased you can look add their filament profile if it is in the list, typically with PLA the Generic option works great, and you can always tweak the settings if things are not coming out correctly.
7. Updates: Defaults will suffice. Alt + n.
8. Reload from disk: Defaults will suffice. Alt + n.
9. Files Association: We recommend checking both boxes so Windows will launch Prusa Slicer if you open a STL or .3mf (Prusa project) file. Alt + n.
10. View Mode: Defaults will suffice. Alt + f.

### Setting up Preferences for Low Vision
We recommend setting up some of the following slicer preferences to enable more efficient low vision access.
<br><br>

1. Launch preferences (alt c > p or control + p) and under General Preferences, make sure the following options are checked or unchecked (in addition to the defaults already checked):
  - Auto-center parts
  - Allow just a single PrusaSlicer instance: so you don't start too many windows of PrusaSlicer
  - **UNCHECK** Ask for unsaved changes in project
  - **UNCHECK** Ask to save unsaved changes in presents  when closing the application or when loading a new project
  - **UNCHECK** Ask for unsaved changes in presents when selecting new preset
  - **UNCHECK** Ask for unsaved changes in presents when creating a new project
  - **UNCHECK** Show splash screen
2. Change to the GUI tab in preferences, make sure the following options are checked or unchecked(in addition to the defaults already checked):
  - Use colors for axes values in Manipulation panel (will highlight the XYZ options in the right sidebar for manipulating an object, a model has to be loaded to see the Manipulation panel, optional if the contrast works for you)
  - Set settings tabs as menu items (experimental) - **this is one of the most important preferences it enables accessing the different settings windows via the windows menu (alt)**
  - **UNCHECK** Show "Tip of the day" notification after start
  - Use custom size for toolbar icons
3. Change to the Dark mode (experimental) tab in preferences, make sure the following options are checked or unchecked:
  - Enable dark mode (optional but recommended for most LV users)
<br><br><br>

## Resources
- [Download Prusa Slicer](https://www.prusa3d.com/page/prusaslicer_424/)
<br><br><br>
