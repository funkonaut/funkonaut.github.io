---
layout: post
title:  "Fab Lab 3D Printing: Prusa Slicer Setup and Use (For LV Users)"
date:   1113-01-02
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
In this lesson you will learn how to set up and use the Prusa Slicer software (GUI). The graphical user interface for Prusa Slicer is not fully accessible but has several keyboard shortcuts and features that make enables efficient low vision access. After you have sliced your model we will briefly go through steps on how to print it using a Prusa Mk3S printer. 
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
3. Choose where to install the program files we recommend the default location, if you choose another location make sure you make note because you will need the path to the CLI .exe file if you want to add the CLI to your PATH environment variable. Alt + n for next page.
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

## Using Prusa Slicer GUI
We recommend trying out the CLI Prusa Slicer set up in the previous tutorial at least learning about how to use the CLI interface is a helpful learning experience. If you do not have basic command line shell skills down you can solely use the GUI, most users use the GUI, there is no shame in only using the GUI, its just not very [1337...](https://en.wikipedia.org/wiki/Leet). Additionally while the GUI is not accessible a screen reader user can use it for very basic slicing using the keyboard shortcuts. The basic workflow is as follows:
<br><br>

1. Import a STL file (ctrl + i)
2. On the right side of the screen is a side bar where you can load installed configuration profiles. You can click on the top drop down menu to focus the side bar and then tab navigate between the options:
  - The first drop down menu is print settings it specifies things like layer height and print speed, the larger the layer height the less print time 
  - The next drop down menu is filament settings, here you can select the Generic PLA filament profile you may have installed in the configuration wizard
  - The next drop down menu is the printer settings, here you can select the printer profile you installed our printer is a Prusa MK3s
  - The next drop down menu is the Supports settings, here you can decide if you would like to include supports in your model, due to the nature of FFF 3D printers anything on your print with a greater then 50 degree overhang will need a support, if you need to use supports we recommend just placing them "everywhere" when you are starting.
  - The next drop down menu is the infill setting, this is the amount of material that fills the inside of your model typically 20% is good, 50% for a more durable model, and a 100% for a solid model (this will increase print time and material usage) 
3. Now lets position and move our model. On the side bar under the settings drop down menus is a table with the different models you have imported into Prusa Slicer, you can select them here or by clicking them in the plater window (the large area to the left where your model sits)
  - You can adjust the position, rotation, scale, and size for each of the X, Y, Z dimensions of your model by typing in the text boxes in this list. 
  - You can also use the plater view and your mouse or arrow keys to adjust your model, you can select the tools in the side bar on the left side of the screen or with keyboard shortcuts: 
  - The default tool is the move tool (m)
  - the scale tool (s) will allow you to scale your model
  - the rotate tool (r) will allow you to rotate your model
  - the place on face tool (f) will allow you to click a face of your model and anchor it to the print bed, its helpful to use in place of rotating if you want your model in a different orientation.
4. When your model(s) slicer settings are selected and it is positioned and sized correctly on the build plate (plater) you can slice the model by clicking the "slice now" button in the bottom right area of the screen or by pressing ctrl + r
5. After your model is sliced you will see stats about the print appear in the right sidebar including the estimated filament used (in grams) and the print time. You can click the "Export G-code" button or press ctrl + u which will launch a Windows file dialogue where you can save your G-code file on an external SD card.
6. You can now print your model by plugging in your SD card into the 3D printer and selecting the file you just uploaded.
<br><br>

### Helpful Keyboard Shortcuts for Prusa Slicer
The following keyboard shortcut tables are a modified from [Prusa Slicers website](https://help.prusa3d.com/article/keyboard-shortcuts_1764). Each subheading is for each Window View available in the Prusa Slicer GUI.
<br><br>

#### Main Window / Commands Keyboard Shortcuts

| Shortcut            	| Description   	| 
|---------------------	|---------------	| 
| control + shift + v 	| view all      	| 
| control + 4         	| top view      	| 
| control + 5         	| bottom view   	| 
| control + 6         	| left view     	| 
| control + 7         	| right view    	| 
| control + 8         	| front view    	| 
| control + 9         	| back view     	| 
| control + 0         	| diagonal view 	| 
| control + [         	| zoom out      	| 
| control + ]         	| zoom in       	| 
<br><br>

#### Plater Keyboard Shortcuts

| Keyboard Shortcut        	| Description                                   	| 
|--------------------------	|-----------------------------------------------	| 
| A                        	| Arrange                                       	| 
| Shift + A                	| Partial arrange (arrange selection)           	| 
| +                        	| Add instance of selected object               	| 
| -                        	| Remove instance of selected object            	| 
| M                        	| Move                                          	| 
| S                        	| Scale                                         	| 
| R                        	| Rotate                                        	| 
| C                        	| Cut                                           	| 
| F                        	| Place on Face                                 	| 
| L                        	| SLA supports                                  	| 
| H                        	| SLA hollowing                                 	| 
| Page Up                  	| Rotate selection by 45 degrees CCW            	| 
| Page Down                	| Rotate selection by 45 degrees CW             	| 
| Arrow Left/Right/Up/Down 	| Move by 10mm                                  	| 
| Shift + Any arrow key    	| Movement step set to 1mm                      	| 
| Ctrl + Any arrow key     	| Movement in camera space                      	| 
| Ctrl + Mouse click       	| Add object to current selection               	| 
| Shift+ Mouse drag        	| Box selection                                 	| 
| Alt+ Mouse drag          	| Box deselect                                  	| 
| Shift + Scale tool       	| Snap by 5%                                    	| 
| Shift + Move tool        	| Snap by 1 mm                                  	| 
| F+ Scale tool            	| Scale to fit (maximum scale)                  	| 
| Ctrl+ Scale tool         	| Scale only in one direction                   	| 
| K                        	| Change camera type (perspective/orthographic) 	| 
| B                        	| Zoom to bed                                   	| 
| Z                        	| Zoom to all objects                           	| 
| Z+ Selected model        	| Zoom to selected model                        	| 
| I                        	| Zoom in                                       	| 
| O                        	| Zoom out                                      	| 
| Shift + Tab              	| Collapse/Expand the sidebar                   	| 
| Ctrl + M                 	| Show/hide 3D connexion device settings        	| 
| 0- 6                     	| Camera view                                   	| 
| E                        	| Show/hide object/instance labels              	| 
| Shift + ?                	| Show keyboard shortcuts                       	| 
| Ctrl+ Mouse click        	| Show/hide 3D connection device settings       	| 
<br><br>

#### Preview Keyboard Shortcuts

| Keyboard Shortcut 	| Description                                	| 
|-------------------	|--------------------------------------------	| 
| Arrow Up or W     	| Move active end of vertical slider up      	| 
| Arrow Down        	| Move active end of vertical slider down    	| 
| Arrow Left        	| Move active end of horizontal slider left  	| 
| Arrow Right       	| Move active end of horizontal slider right 	| 
| L                 	| Show hide legend                           	| 
| Del               	| Delete selected                            	| 
| Ctrl+Del          	| Delete All                                 	| 
<br><br><br>

## Review
In this lesson you learned:
- How to install and set up the GUI version of Prusa Slicer for LV access
- The basic graphical layout of the GUI version of Prusa Slicer
- How to use the GUI version of Prusa Slicer to slice and 3D print a model
- Helpful keyboard shortcuts for the GUI version of Prusa Slicer
<br><br><br>

## Resources
- [Download Prusa Slicer](https://www.prusa3d.com/page/prusaslicer_424/)
- [Prusa Slicers keyboard shortcut documentation](https://help.prusa3d.com/article/keyboard-shortcuts_1764)
<br><br><br>
