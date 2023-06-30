---
layout: post
title:  "2D to 3D Design in OpenSCAD Using Linear Extrusions"
date:   1111-03-04
last_modified_at: 2023-06-30
categories: [OpenSCAD]
tags: [Lesson 3]
---

<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}

<br><br>

## Learning Objectives
At the end of this lesson, you will be able to:
1. Understand and apply the concept of linear extrusion in OpenSCAD.
2. Use linear extrusion to transform a 2D model into a 3D model.
3. Combine extruded objects with other 3D primitives.
<br><br><br>

## Introducing Linear Extrusion in OpenSCAD
In OpenSCAD, you can convert 2D models into 3D models by adding a third dimension, Z, using the `linear_extrude` operator. This operator accepts a positive parameter that corresponds to the distance the 2D model is extruded along the Z axis. For example:

```OpenSCAD
linear_extrude(5){
    square(10, center=true);
}
```
<br><br>

## Using Linear Extrusion with 2D Models
You can pass any 2D primitive or combination of 2D primitives to the `linear_extrude` operator. This allows for the creation of complex 3D models from simple 2D shapes. For instance:

```OpenSCAD
linear_extrude(5){
  difference(){
    square(10,center=true);
    square(8,center=true);
  }
}
```
<br><br>

## Combining Extruded Shapes with 3D Primitives
Once a 2D model is extruded into 3D, it can be combined with other 3D primitives. However, keep in mind that you cannot properly combine 2D and 3D shapes, or extrude a 3D shape. Here is an example:

```OpenSCAD
difference(){
  linear_extrude(5){
      square(10, center=true);
  }
  cube([5,5,11], center=true);
}
```
<br><br><br>

## Practice Exercises
Now, let's apply what you've learned with these exercises:

1. Use `linear_extrude` and your 2D primitives to create a cylinder of width 3 and height 10.
2. Use `linear_extrude` along with at least one 2D primitive and one 3D primitive to create a ring.
3. Utilize `linear_extrude` to craft a 3D keychain with your name as a raised surface on it.
4. As a bonus, create a module that generates a 3D text shape. This module should accept a string input parameter and a text thickness parameter.
<br><br><br>

## Review
In this lesson, you learned how to:
- Use the `linear_extrude` operator in OpenSCAD.
- Convert a 2D model into a 3D model by adding the Z dimension.
- Combine extruded objects with other 3D primitives.
<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_