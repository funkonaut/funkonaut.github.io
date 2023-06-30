---
layout: post
title:  "3D Primitives: Hello Cube"
date:   1111-01-02
last_modified_at: 2023-01-12
categories: [OpenSCAD]
tags: [Lesson 1]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

## Learning Objectives
Typically when one is learning how to program they begin with a "Hello World" activity where one programs the text "Hello World" to appear on the screen. Since we are working with 3D models we will start with a simple alternation on "Hello World", "Hello Cube". We highly recommend you review the [terminology text file](DO-THIS.com) now so we are all on the same page with technical terminology (don't worry if some words and their definitions are unclear right now we will address them all in further lessons).
<br><br>

In addition to programming your first model you will also learn about navigating the OpenSCAD app and it's different windows. If you followed out recommended setup you should be able to launch OpenSCAD and it will default you to a new code file "Untitled," if OpenSCAD opens to a dialogue go ahead and tab navigate to the "New" button to create a new file. 
<br><br><br>

## The Editor Window
The editor window is where you write your code. Whenever you open a OpenSCAD file or create a new file your focus will be defaulted to this window where you can type your code. To return focus to the editor window at any time you can navigate to the menu bar (alt) first letter navigate to the "Window" menu (w) and first letter navigate to the "Editor" (e) option.
<br><br>

**Important note: if you are using a screen reader and OpenSCAD ever stops reading to you hit alt to focus the menu bar and then escape to return focus back to the editor window and it should start reading again**
<br><br><br>

## Your First Model
While you are in the editor window lets go ahead and type our first line of code:
<br>

`cube(1);`
<br>

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

We now have a larger cube in the preview window (apologies but, take my word for all of this if you can not see the preview window). We just changed the side length for our cube. What happens if we change it to something even larger say 1000? You may notice that only a portion of our cube is displayed in the preview window. This is because while our cube changed our view did not. 
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

<br><br>

## The Error Window
Now lets see what happens when you get something wrong. Change your code to read an incorrect command say:
<br>

`cue(500);`
<br>

Notice you will either not see your design change in the preview window, or if you are using a screen reader you will here "error-log window table warning...". The error-log is a window (default position is in the lower right portion of the screen) that will have a table with the errors or warnings that show up when you try to preview or render your code. You can navigate to the window to here what the warning or error is by navigating to the "Window" menu and then navigating to error-log (alt > w > l).
<br><br><br>

### The Error Table
The error Table is organized into 4 columns: Group, File, Line, Info. You can tab navigate through the different cells. The group column will display Warning or Error. The file column will display the file name, or nothing if there is no file name, line will display the line number causing the warning or error, it will sometimes be blank (we will discuss why later), and the info column will have an info message about why the warning or error is happening.  
<br><br><br>

### Warnings Vs. Errors
Warnings will preview but incorrectly and errors will cause OpenSCAD to not preview. Errors are usually are related to your codes syntax, such as forgetting a semi-colon or argument. Warnings are a bit trickier, for example  you might misspell a shape command this would not be an error (for reasons we will discuss later), but would be a warning. That is why it is important to read the error-log if you get any warnings or errors.
<br><br><br>

## Comments: Single Line and Multiline
Now we will learn about a very important concept in coding, the comment. A comment is a command that lets the computer know to ignore code that follows. Comments in OpenSCAD can be either a single line comment or  a comment block. A single line comment will begin with `//` everything on the same line that follows the `//` will be ignored by the computer. A multiline comment block will begin with `/*` and end with `*/` everything in between the `/*` and `*/` will be ignored by the computer 
<br><br>

Comments are important to add notes or directions to your code. It is always important to add notes or document your code so future you or someone else who is reading your code will better understand (or remember!) how your code works. Try adding a single line comment in front of your cube code: `//cube(1);` and preview it (f5) notice how nothing was shown, that is because the computer is now ignoring your cube command.
<br><br>

If you want to comment out multiple lines but don't want to type `//` infront of every line you can use a comment block. Try deleting your single line comment and surround your cube code with a multiline comment symbols:
<br>
```c
/*
cube(1);
Anything else you write here 
No matter what line it is on
is ignored by the computer...
*/
```
<br><br><br>

## Previewing, Rendering and Exporting
So far we have only been previewing our cube, but in order to get our models out of OpenSCAD we need to render them and export them. Rendering is the process of turning the programmatic description of your model into the image of that model. Exporting is the process of taking that image model and generating a file that is able to be used in other programs. You can render your code by pressing f6, you will here a "bling" if your code renders successfully, and export your code by press f7. 
<br><br>

Exporting your code will bring up a file dialogue so you can determine where you would like to save your file and what you would like to name it as. Export will default to naming your file what your code is named, and exporting it as a STL file type. We won't get into the other types of files for 3D models right now, but STL models are the ones we typically use for 3D printing. You can also access the export feature in the file menu (alt > f > x) if you want to export as another file type.
<br><br>

When you preview your model you are using OpenSCAD's program to show the image of your model very quickly, this is fine for working in OpenSCAD and developing your code, but previewed models can not be used in other programs. For that you have to render and export. Rendering and Exporting are two different steps and keyboard shortcuts in OpenSCAD even though the process is usually done together, that is because sometimes you will find issues with your code that happen in the rendering phase but not the preview phase. 
<br><br>

For instance type the code that gave us a warning: `cue(500);` When we press f6 we get an additionally warning to the one we got when we previewed the code. Try it out, you should here a bling, unfortunately there will not be an auditory cue that the second warning showed up but the second entry in the error-log read something like "No top level geometry rendered." This warning is the typically what you would run into and means that there is no model in OpenSCAD's render so you would just be exporting an empty file. This is why it is important to check you error-log after rendering but before exporting to make sure there are no warnings as warnings will still allow your code to render, but incorrectly.
<br><br><br>

## Next Steps
Now that you have become acquainted with the OpenSCAD application and have created your first shape, we recommend that you read through our [lessons on 3D printing](LINK LESSONS!!!!) so you can begin making your designs come to life! Once you complete the 3D printing lessons you can give [Project 1](LINK PROJECT 1!!!!) a go.  
<br><br><br>

## Review
In this lesson you learned:
- How to create, preview, render, and export a simple cube of different sizes in OpenSCAD.
- How to navigate the different OpenSCAD windows: Editor, Preview, and Error Log.
- How to comment and uncomment line(s) of code in OpenSCAD and why you would want to do such.
<br><br><br>

## Resources
- [OpenSCAD terminology](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/terminology.txt)
- [Your first cube exercises](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%201/1_0_intro_to_openscad_student.scad)
<br><br><br>