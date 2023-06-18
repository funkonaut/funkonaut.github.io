---
layout: post
title:  "OpenSCAD Lesson 2.1: Difference"
date:   1111-02-01
last_modified_at: 
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
- Understand how to use the difference() function in OpenSCAD.
- Learn how to create complex shapes using boolean operations.
- Understand how to create and position holes within objects.
- Gain experience working with different geometrical shapes like cube, cylinder, and sphere.

## Exploring Boolean Operations in OpenSCAD
In this lesson, we will explore a powerful tool in OpenSCAD - the difference() function. It allows us to subtract one shape from another, creating a wide variety of complex objects from simple geometrical shapes.

OpenSCAD uses a coordinate system to position shapes. This can be understood as a 3D grid with x, y, and z axes. When placing shapes or moving them around, we specify where they should go in relation to this grid. Visualizing this may be challenging for some, so we recommend using a tactile coordinate system, like an APH Graph Board, to help understand it.
<br><br>

## Understanding difference() Function
In OpenSCAD, the difference() function works by subtracting subsequent shapes (or groups of shapes) from the first shape listed in the difference block. This subtraction is based on the volume of the shape, rather than its surface.

A simple example of the difference function is shown below:

```
difference() {
cube([10, 10, 10]);
cylinder(h=10,r=2);
}
```

In this example, a cylinder is subtracted from a cube, resulting in a cube with a cylindrical hole.
<br><br><br>

## Practical Applications of difference() Function
Let's go through a few practical examples where you can apply the difference() function:

- To create a box without a lid:

``` 
h = 10;
w = 20;
l = 30;
t = 2;
difference() {
  cube([l,w,h],center = true);
  translate([0,0,t])
    cube([l-t*2,w-t*2, h],center = true);
}
```

- To create a cup:

```
h = 50;
d = 40;
t = 2;
difference() {
  cylinder(h = h,d = d,center = true);
  translate([0,0,t])
    cylinder(h = h,d = d-t*2,center = true);
}
```
<br><br>

## Review
In this lesson you learned:
- The concept of the difference() function in OpenSCAD.
- How to create complex objects using simple geometric shapes and boolean operations.
- How to position and translate objects within the coordinate system.
- The use of difference() function in creating everyday objects like a box and a cup.

<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%202/2_2_bool_diff_student.scad)
- [OpenSCAD User Manual: Boolean operations](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/Boolean_Operations)

<br><br><br>