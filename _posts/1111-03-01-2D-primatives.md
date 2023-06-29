---
layout: post
title:  "2D Design in OpenSCAD: Working with Primitives, Booleans, and Transformations"
date:   1111-03-01
last_modified_at: 2023-06-28
categories: [OpenSCAD]
tags: [Lesson 3]
---
<br>

## Contents
{:.no_toc}
{:toc}
<br><br>

## Learning Objectives
At the end of this lesson, you will be able to:
1. Understand the basics of 2D design in OpenSCAD.
2. Create 2D primitives: square and circle.
3. Use transformations and Boolean operations for 2D designs.
<br><br><br>

## Introduction to 2D Design in OpenSCAD
In this lesson, we will delve into 2D design with OpenSCAD, a technique useful for creating cut or SVG files for the laser cutter. You'll find that 2D design in OpenSCAD shares many similarities with 3D design.
<br><br>

## Creating 2D Primitives: Square and Circle
OpenSCAD offers four main primitives for 2D design: square, circle, polygon, and text. We will explore the square and circle in this lesson. Remember, like their 3D counterparts, OpenSCAD's square and circle primitives may not exactly match their mathematical definitions.

For instance, let's explore the **square** primitive:

```OpenSCAD
square(10);
```

This line creates a square with a side length of 10 units. By adding the `center=true` flag, we can center the square in our workspace. Alternatively, we can define a square with differing width and height:

```OpenSCAD
square([5,20], center=true);
```

You can try creating a rectangle that is 2 units by 10 units. When you preview (F5) and render (F6) the shape, you might notice visual differences. To export a 2D design, choose `File > Export > Export as SVG` (Alt+F+X+V, Enter).

Let's turn to the **circle** primitive:

```OpenSCAD
circle(r=10);
```

This line generates a centered circle with a radius of 10 units. Now, you can experiment with creating a circle that is 30 units wide.
<br><br><br>

## Transformations and Booleans for 2D Designs
The exciting aspect of 2D design is combining primitives with transformations and Boolean operations, such as `translate`, `union`, and `difference`. 

For example, the following code creates a wheel with a circular mounting hole:

```OpenSCAD
difference(){
    circle(10);
    circle(1);
}
```

Feel free to modify the code to create a "wonky wheel" with a slightly off-center mounting hole.
<br><br><br>

## Practice Exercises
1. Create a wheel with a square axis hole:

```OpenSCAD
wheel_size = 10;
axis_size = 1;
difference(){
 circle(d=wheel_size);
 square(axis_size,center=true);
}
```

2. Design a picture frame:

```OpenSCAD
frame_size = 50;
border_w = 10;
difference(){
 square(frame_size,center=true);
 square(frame_size-border_w*2,center=true);
}
```

3. Make a 4x4 grid of wheels:



```OpenSCAD
wheel_size = 10;
axis_size = 1;
offset = 2;
for(x = [1:4]){
 for(y = [1:4]){
  translate([(wheel_size+offset)*x,(wheel_size+offset)*y,0])
  difference(){
   circle(d=wheel_size);
   square(axis_size,center=true);
  }
 }
}
```

4. Design a picture frame with a mounting hole:

```OpenSCAD
frame_size = 50;
border_w = 10;
hole_size = 2;
difference(){
 difference(){
  square(frame_size,center=true);
  square(frame_size-border_w*2,center=true);
 }
 translate([0,frame_size/2-border_w/2,0])
 circle(hole_size);
}
```
<br><br><br>

## Review
In this lesson you learned:
- The fundamentals of 2D design in OpenSCAD.
- How to create 2D primitives, specifically the square and circle.
- How to use transformations and Boolean operations in 2D designs.
<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%203/3_3_2D_Design_Student.scad)
<br><br><br>