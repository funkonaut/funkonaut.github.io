---
layout: post
title:  "Boolean Operations: Combining Shapes with Intersections"
date:   1111-04-02
last_modified_at: 2023-06-30
categories: [OpenSCAD]
tags: [Bonus]
---
<br>

## Learning Objectives
By the end of this lesson, students should be able to:
1. Understand the concept of intersection in OpenSCAD.
2. Know how to use the `intersection` function and its parameters.
3. Create complex 3D shapes by intersecting simple shapes.

<br><br>

## Intersecting Shapes in OpenSCAD
The `intersection` function in OpenSCAD allows you to find the common volume of two or more 3D shapes. This function operates on all its children in the order of their definition. That is, it intersects the first shape with the second, then the result of that intersection with the third, and so forth. This is an important tool in creating complex objects from simpler shapes.

Remember, the resulting shape will only include the regions where every child shape overlaps. This means that any part of a shape that does not intersect with every other shape will be excluded.

<br><br><br>

## Creating Complex Shapes with `intersection`
The following examples show how you can use `intersection` to create various complex 3D shapes.

1. Quarter of a sphere:

```OpenSCAD
intersection() {
  sphere(5);
  translate([-10,0,0])
  cube([10, 10, 10]);
}
```
2. Quarter of a cylinder:

```OpenSCAD
intersection() {
  cylinder(r=5,h=5,center=true);
  cube([10, 10, 10]);
}
```
3. Half of a cylinder:

```OpenSCAD
intersection() {
  cylinder(r=5,h=5,center=true);
  translate([0,5,0])
  cube([10, 10, 10],center=true);
}
```
4. Two quarters of a cylinder in adjacent octants:

```OpenSCAD
intersection() {
  cylinder(r=5,h=5,center=true);
  union(){
    cube([10, 10, 10]);
    translate([-10,-10,0])
    cube([10, 10, 10]);
  }
}
```
You can use intersections to make more complex shapes with rounded corners by intersecting overlapping cubes and spheres. As a bonus, try to make a dice by intersecting a cube and a sphere.

<br><br><br>

## Review
In this lesson, you learned:
- The concept of intersection in OpenSCAD.
- How to use the `intersection` function to find the common volume of two or more 3D shapes.
- How to create complex 3D shapes by intersecting simple shapes.

<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%202/2_4_intersection_student.scad)
- [OpenSCAD Intersection Documentation](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/The_OpenSCAD_Language#intersection)
<br><br><br>