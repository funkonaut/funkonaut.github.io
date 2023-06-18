---
layout: post
title:  "OpenSCAD Lesson 1.6: Translate"
date:   1111-01-06
last_modified_at: 2023-06-17
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
- Learn to use the 'center' parameter to modify the placement of shapes.
- Understand how to use 'translate' to move shapes within the modeling space.
- Understand spatial orientation in OpenSCAD's 3D space.

## Centering and Translating Shapes
In OpenSCAD, the 'center' parameter is used to control whether the origin of the shape is at its center or at its bottom corner. This plays a vital role in the placement of your 3D model.

```
cube([20, 10, 10],center=true);
cylinder(h=20,r=5,center=true);
```

The 'translate' function moves the object from its original location to a new location in the 3D space. Here's an example:

```
translate([-10, 20, 0]) cube([20, 10, 10]);
translate([-10, 20, 0]) sphere(r=10); 
```
<br><br>

## Understanding 3D Space and Movement
OpenSCAD's 3D space is divided into eight octants, each defined by the combination of the signs of the X, Y, and Z coordinates. Here's how you can move shapes into different octants:

```
//Moving a centered cube to the first octant
translate([5,5,5])
cube(10,center=true);

//Moving a centered cylinder to the third octant
translate([-5,-5,5])
cylinder(h=10,d=10,center=true);

//Moving a centered cone to the seventh octant
translate([-5,-5,-5])
cylinder(h=10,d1=10,d2=0,center=true);
```
<br><br><br>

## Practice: Creating Complex Shapes
Now that you understand the basics of moving shapes in OpenSCAD's 3D space, let's create a couple of complex shapes:

1. Mickey Mouse Shape:

```
cylinder(h=1, r= 3, center=true);
translate([-2,2,0])
cylinder(h=1, r= 2, center=true);
translate([2,2,0])
cylinder(h=1, r= 2, center=true);
```

2. Yo-Yo Shape:

```
translate([0,0,-2])
cylinder(h=20, r1 = 20, r2 = 0, center=true);
translate([0,0,2])
cylinder(h=20, r1= 0, r2 = 20, center=true);
```
<br><br><br>

## Review
In this lesson, you learned:
- How to use the 'center' parameter to control the placement of shapes in OpenSCAD.
- How to use the 'translate' function to move objects within the 3D space.
- The concept of 3D space orientation and movement across different octants.
- How to create complex shapes by manipulating and combining basic shapes.

<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%201/1_2_shape_mods.scad)
- [OpenSCAD User Manual: Transformations](https://en.wikibooks.org/wiki/Open)