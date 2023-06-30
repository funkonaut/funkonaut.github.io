---
layout: post
title:  "Boolean Operations: Difference"
date:   1111-02-04
last_modified_at: 2023-06-29
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
In this lesson, we will explore a powerful tool in OpenSCAD - the difference() function. OpenSCAD calls the difference function and other functions like it "Boolean Operations." This refers to how the shape is processed behind the scenes in OpenSCAD where overlapping portions of shapes are marked either true or false, if that doesn't make a whole lot of sense that is okay just know that when we refer to boolean operations we are talking about combing shapes in different ways. The difference function allows us to subtract one shape from another, creating a wide variety of complex objects from simple geometrical shapes.
<br><br>

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

In this example, a cylinder is subtracted from a cube, resulting in a cube with a cylindrical hole. If we were to continue adding shapes in between the curly brackets each shape would be subtracted from the subsequent result. For instance:

```
difference() {
cube([10, 10, 10]);
cylinder(h=10, r=2);
translate([0,0,1])
cylinder(h=5, r=3);
}
```

Subtracts a cylinder from a cube and then subtracts a smaller in height but wider cylinder that has been moved up 1 from the result.
<br><br><br>

## Practical Applications of difference() Function
Let's go through a few practical examples where you can apply the difference() function:

- To create a box without a lid:

``` 
difference() {
  cube([30,20,10], center = true);
  translate([0,0,2]) //translate up a thickness amount so the box has a bottom
    cube([30-2*2,20-2*2, 10], center = true); //create a smaller box hole that is smaller by the thickness of the box (2 edges so we will subtract two thickness amounts i.e. 2*2)
}
```

- To create a cup:

```
difference() {
  cylinder(h = 50,d = 40, center = true);
  translate([0,0,2]) //translate up a thickness amount so the cup has a hole
    cylinder(h = 50, d = 40-2*2, center = true); //create a smaller cylinder so your cup is hollow (2 edges so we will subtract two thickness amounts i.e. 2*2)
}
```
<br><br>

You may be wondering why we made our negative shapes (the shapes that come second in the d)
<br><br><br>

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