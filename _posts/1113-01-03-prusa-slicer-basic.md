---
layout: post
title:  "Fab Lab 3D Printing: Prusa Slicer Basic Use (GUI)"
date:   1113-01-03
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
In this lesson you will learn how to use some of the basic features of the Prusa Slicer software to make your first 3D print. The graphical user interface for Prusa Slicer is not fully accessible but has several keyboard shortcuts and features that enables efficient low vision access and basic slicing can be achieved for screen reader users. 
<br><br><br>

## Pre-Requisites 
- basic Windows navigation
- basic folder and file navigation in Windows
<br><br><br>

## Steps for Basic Printing
In order to use Prusa Slicer to slice a model (prepare it for 3D printing) follow these steps:
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
  - a helpful tip is that you can auto arrange multiple imported models by selecting them all (ctrl+ a) and then hitting the auto-arrange tool hot key (a).
4. When your model(s) slicer settings are selected and it is positioned and sized correctly on the build plate (plater) you can slice the model by clicking the "slice now" button in the bottom right area of the screen or by pressing ctrl + r
5. After your model is sliced you will see stats about the print appear in the right sidebar including the estimated filament used (in grams) and the print time. You can click the "Export G-code" button or press ctrl + u which will launch a Windows file dialogue where you can save your G-code file on an external SD card.
6. You can now print your model by plugging in your SD card into the 3D printer and selecting the file you just uploaded.
<br><br>


### Helpful Keyboard Shortcuts for Prusa Slicer
The following keyboard shortcut tables are a modified from [Prusa Slicers website](https://help.prusa3d.com/article/keyboard-shortcuts_1764). Each subheading is for each Window View available in the Prusa Slicer GUI.
<br><br>

#### Main Window / Commands Keyboard Shortcuts
  
| Shortcut            	| Description   	| 
|---------------------|---------------| 
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
<br>
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
<br>
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
 - import (ctrl + i)
 - slice (ctrl + r)
 - export (ctrl + u)
 - print (3D printer specific)
- Helpful keyboard shortcuts for the GUI version of Prusa Slicer
<br><br><br>

## Resources
- [Download Prusa Slicer](https://www.prusa3d.com/page/prusaslicer_424/)
- [Prusa Slicers keyboard shortcut documentation](https://help.prusa3d.com/article/keyboard-shortcuts_1764)
<br><br><br>
