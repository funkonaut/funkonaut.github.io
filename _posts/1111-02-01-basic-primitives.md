---
layout: post
title:  "OpenSCAD Lesson 2.1: Basic Primitives"
date:   1111-02-01
last_modified_at: 2023-01-12
categories: [OpenSCAD]
tags: [Lesson 2]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

## Learning Objectives
Before starting this lesson, it is recommended that students review the terminology listed in the "terminology.txt" file. It is also important to review the XYZ coordinate system and the different windows in the program such as the preview and editor windows.
<br><br>

In this lesson, we will be creating basic 3D primitives using OpenSCAD. As you might remember from the terminology text file, primitives are how we build our models in OpenSCAD, the word is synonymous with base shape. 
<br><br><br>

# Primitive Shape Commands in OpenSCAD
In order to understand how commands work in OpenSCAD lets take a look at our first OpenSCAD shape `cube(1);` Go ahead and write the code for a cube and preview it (remember to preview the shape, hit f5.)
<br><br>

A shape command is made up of multiple parts: 
<br>
1. The name of the shape command: "cube"
2. The parameters that defines the shape "1" 
3. The semi-colon at the end of the shape command. 
<br><br>

Since shape commands in OpenSCAD end with a semi-colon, the number of spaces in the code does not matter, as long as it does not change the name or value of a command or parameter. For example `cube(1 );` is the same as `cube (1);` but `cub e(1);` will not work as it changes our command name. 
<br><br><br>

## Parameters 
We will start by creating a cube. Notice how the shape's corner is at the origin (0,0,0) or the center. We can change the numbers in the brackets [] to see how the shape grows or shrinks. The brackets [] are used to designate a vector. For example, the following code creates a cube with the dimensions of 5, 10, and 20:


cube([5,10,20]);
It is good practice to place the cube so that its center is at the origin, which can be done by using the center flag (a flag is a true or false parameter). The following code creates a cube with the dimensions of 5, 10, and 20, and centers it at the origin:


cube([5,10,20],center=true);
Creating a Sphere
Next, we will create a sphere. The sphere only requires one measurement, the radius, and it is centered around the origin. The resolution of 40 is good enough for most cases. The following code creates a sphere with a radius of 10:


$fn = 40;
sphere(r=10); 
Creating a Cylinder
We will also create a cylinder. The cylinder requires three measurements: the height (h), the radius of the top (r1), and the radius of the bottom (r2). It is good practice to label the parameters, as shown in the following example:


cylinder(h=20,r1=5,r2=5); 
But it is also possible to not label them and just list the measurements in the order of height, r1, and r2 like the following example:


cylinder(20,5,5); 
Creating a Cone
We can also create a cone, which is similar to a cylinder but with different radii for the top and bottom. Cylinders are centered around the Z axis and touching the xy plane. The following code creates a cone with a height of 20, a radius of 5 at the top and a radius of 2 at the bottom:


cylinder(h=20,r1=5,r2=2); 
We can also create a pointed cone by setting the radius of the bottom to 0:


cylinder(h=20,r1=5,r2=0); 
Another way to make a cylinder is by setting only one radius like this:


cylinder(h=20,r=5); 
Practice
For practice, we will create a top and a stair step. The following code creates a top with
## Section Title Case 
PARAGRAPH
<br><br>
PARAGRAPH
<br><br><br>

## Section
TEXT:
- BULLET OR NUMBERED LIST
<br><br><br>


## Review
In this lesson you learned:
- 
<br><br><br>

## Resources
- []()
<br><br><br>