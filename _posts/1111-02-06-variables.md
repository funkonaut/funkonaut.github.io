---
layout: post
title:  "Coding Fundamentals: Variables and Parametric Programming"
date: 1111-02-06
last_modified_at: 2023-06-30
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
- Understand the concept of variables in OpenSCAD.
- Learn how to declare and assign values to variables.
- Understand how to use variables to create parameterized models.
- Learn about mathematical operations on variables.

## Understanding Variables
In OpenSCAD, a variable is a named place to store a value. Variables are useful when you want to repeat the same value in multiple places in your script or adjust a single value to modify your 3D model dynamically.

Variables in OpenSCAD must start with a letter, and they cannot have spaces. For example, `var = 10;` declares a variable named `var` and assigns it a value of `10`.
<br><br>

## Declaring and Using Variables
To make the concept more meaningful, let's declare variables `w_cube`, `l_cube`, and `h_cube` representing the width, length, and height of a cube:

```
w_cube = 10;
l_cube = 20;
h_cube = 5;
```
You can use these variables to define a cube:

```
cube([w_cube,l_cube,h_cube], center=true);
```
<br><br><br>

## Parametric Programming and Mathematical Operations
You can perform mathematical operations on variables to modify the dimensions of your shapes dynamically. For example, you can create a cylinder that is half the height and twice the width of the cube:

```
h_cyl = h_cube/2;
w_cyl = 2*w_cube;

translate([0,0,h_cyl/2+h_cube/2]) // positioning the cylinder on top of the cube
cylinder(d= w_cyl, h=h_cyl, center=true);
```

By adjusting the variables, you can change the shapes' dimensions without having to rewrite your entire script, making your code more flexible and efficient.
<br><br><br>

## Review
In this lesson, you learned:
- The concept of variables in OpenSCAD and how to declare and assign values to them.
- How to use variables for defining the dimensions of your 3D shapes, achieving what is known as parametric modeling.
- How to perform basic mathematical operations on variables to adjust the dimensions of your shapes dynamically.

<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%202/2_0_variables_student.scad)
- [Parameterization practice code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%202/2_1_parameterization_practice_student.scad)
- [OpenSCAD User Manual: Variables](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/Variables_and_Functions)
<br><br><br>