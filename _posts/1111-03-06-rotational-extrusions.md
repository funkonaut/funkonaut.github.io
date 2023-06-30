---
layout: post
title:  "Extrusions: Rotational Extrusions"
date:   1111-03-06
last_modified_at: 2023-06-29
categories: [OpenSCAD]
tags: [Lesson 3]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

---
layout: post
title:  "OpenSCAD Lesson: Rotate Extrude Function"
date:   2023-05-05
last_modified_at: 
categories: [OpenSCAD]
tags: [Coding, 3D modeling, Rotate Extrude]
---
<br>

## Learning Objectives
By the end of this lesson, students should be able to:
1. Understand the concept of rotational extrusion in OpenSCAD.
2. Know how to use the `rotate_extrude` function and its parameters.
3. Understand how transformations can affect the extrusion process.
4. Create simple 3D shapes using rotational extrusion.

<br><br>

## Understanding Rotational Extrusion in OpenSCAD
Rotational extrusion is a key concept in 3D modeling that allows you to create symmetrical solids by spinning a 2D shape around the Z-axis. Think of a potter's wheel; the clay object being shaped on the wheel is the 2D shape you're feeding into the `rotate_extrude` function. Here, OpenSCAD acts as your virtual potter's wheel, rotating your shape about the Z-axis to create a 3D solid. 

It's important to note that `rotate_extrude` works on the projection of the 2D polygon onto the XY plane, and any transformations applied to the 2D polygon before extrusion can change the final 3D object.

<br><br><br>

## How to Use `rotate_extrude` Function
The `rotate_extrude` function spins a 2D shape around the Z-axis to form a solid. Here's a basic example of its usage:

```OpenSCAD
rotate_extrude(convexity = 10)
translate([2, 0, 0])
circle(r = 1);
```
In this example, a circle of radius 1 is translated 2 units along the X-axis and then extruded rotationally to form a torus.

This function also accepts several parameters:
- `angle` (default is 360): Specifies the number of degrees to sweep, starting at the positive X-axis.
- `convexity` (default is 2): Helps with rendering non-trivial 2D shapes.
- `$fa`, `$fs`, and `$fn`: Control the minimum angle, minimum circumferential length, and fixed number of fragments in 360 degrees, respectively.

<br><br><br>

## Improving Mesh Quality
We can improve the quality of our 3D shapes by increasing the number of fragments that make up the 2D shape and the extrusion. 

```OpenSCAD
rotate_extrude(convexity = 10, $fn = 100)
translate([2, 0, 0])
circle(r = 1, $fn = 100);
```
However, keep in mind that increasing these values can also increase render times.
<br><br><br>

## Review
In this lesson, you learned:
- The concept of rotational extrusion in OpenSCAD and how it's like a potter's wheel.
- How to use the `rotate_extrude` function to create 3D objects from 2D shapes.
- How transformations can affect the projection of the 2D shape and the final 3D object.
- How to control the quality of the 3D shape by adjusting fragment values.
<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%202/2_2_bool_diff_student.scad)
- [OpenSCAD Rotate Extrude Documentation](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/Using_the_2D_Subsystem#rotate_extrude)

