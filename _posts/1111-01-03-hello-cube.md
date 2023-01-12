---
layout: post
title:  "OpenSCAD Lesson 1.3: Hello Cube"
date:   1111-01-03
last_modified_at: 2023-01-12
categories: [OpenSCAD]
tags: [Lesson 1]
---
<br><br>

Typically when one is learning how to program they begin with a "Hello World" activity where one programs the text "Hello World" to appear on the screen. Since we are working with 3D models we will start with a simple alternation on "Hello World", "Hello Cube". We highly recommend you review the [terminology text file](DO-THIS.com) now so we are all on the same page with technical terminology (don't worry if some words and their definitions are unclear right now we will address them all in further lessons) 
<br><br>

In addition to programming your first model you will also learn about navigating the OpenSCAD app and it's different windows. If you followed out recommended setup you should be able to launch OpenSCAD and it will default you to a new code file "Untitled," if OpenSCAD opens to a dialogue go ahead and tab navigate to the "New" button to create a new file. 
<br><br><br>

## The Editor Window
The editor window is where you write your code. Whenever you open a OpenSCAD file or create a new file your focus will be defaulted to this window where you can type your code. To return focus to the editor window at any time you can navigate to the menu bar (alt) first letter navigate to the "Window" menu (w) and first letter navigate to the "Editor" (e) option.
<br><br><br>

## Your first model
While you are in the editor window lets go ahead and type our first line of code:
<br><br>

`cube(1);`
<br><br>

Make sure to type it in exactly as how it appears above or will get an error or warning. Now press f5 to preview your code, if you did not hear anything a 1 by 1 by 1 cube should have shown up in the preview window.*
<br><br>

**Note: OpenSCAD is unit-less that means 1 could be 1 inch or 1 millimeter, most 3D printing programs use millimeters as the default unit so we will just assume from now on that OpenSCAD designs are in millimeters*
<br><br><br>

## The Preview Window
The preview window is where your code is previewed. It consist of 3 axis, the X, Y, and Z axis. These are like the Cartesian axis (X and Y axis), but with an added dimension, the Z axis, referred to as height. The X axis is referred to as width and the Y axis as depth.
<br><br>

We can navigate the preview window without the use of a mouse with several keyboard shortcuts. Even if you are using OpenSCAD non visually becoming acquainted with the preview window keyboard shortcuts can be helpful before you learn to 3D print your designs and want a sighted user to describing your model to you. 
<br><br><br>

### Preview Window View Changing Keyboard Shortcuts
Lets practice changing size of our cube and explore some preview keyboard shortcuts to change the view of our preview window:
<br><br>

Change your cube code to `cube(10);` 
<br><br>

We now have a larger cube in the preview window (apologies but, take my word for all of this if you can not see the preview window). We just changed the side length parameter for our cube. What happens if we change it to something even larger say 1000? You may notice that only a portion of our cube is displayed in the preview window. This is because while our cube changed our view did not. 
<br><br>

In order to view the whole shape in the preview window you can use the "View All" keyboard shortcut: **control + shift + v**. Try it, you will see your large cube now centered in the preview window, this will probably be the most useful keyboard shortcut.  
<br><br>

You can adjust the view by using the mouse, scrolling or two finger drag up and down for a touchpad will zoom in and out, a left click and drag will rotate your axis, and right click and drag will translate (move) your axis. This is fine and all but we prefer to use the keyboard shortcuts, they are more efficient and accessible. You can see all the view commands in the View menu (alt > v). 
<br><br>

#### View Changing Keyboard Shortcuts Table
Try out the following helpful View keyboard shortcuts with your large cube!
<br><br>

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

<br><br><br>

## The Error Window
Now lets see what happens when you get something wrong. Change your code to read an incorrect command say:
<br>

`cue(1000);`
<br>

### Warnings Vs. Errors

## The Console Window

## Comments: Single Line and Multiline

<br><br><br>

## Review
In this lesson you learned:
- How to create a simple cube of different sizes in OpenSCAD.
- How to navigate the different OpenSCAD windows: Editor, Preview, Error Log, and Console.
- How to comment and uncomment line(s) of code in OpenSCAD and why you would want to do such.
<br><br><br>

## Resources
- [OpenSCAD Terminology]()
- [Your first cube code])()
- [OpenSCAD keyboard shortcuts list]()
<br><br><br>