---
layout: post
title:  "Primitives: Basic 3D Shapes"
date:   1111-01-04
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
Before starting this lesson, it is recommended that you review the [terminology.txt file](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/terminology.txt). In this lesson, we will be creating basic 3D primitives using OpenSCAD. As you might remember from our terminology and previous lessons, primitives are how we build our models in OpenSCAD, the word is synonymous with base shape. 
<br><br><br>

# Primitive Shape Commands in OpenSCAD
In order to understand how commands work in OpenSCAD lets take a look at our first OpenSCAD shape
```c
cube(1);
```
Go ahead and write the code for a cube and preview it (remember to preview the shape, hit f5.)
<br><br>

A shape command is made up of multiple parts:
<br>

1. The name of the shape command: "cube"
2. The parameter or parameters that defines the shape "1" 
3. The semi-colon at the end of the shape command. 
<br><br>

Since shape commands in OpenSCAD end with a semi-colon, the number of spaces in the code does not matter, as long as it does not change the name or value of a command or parameter. For example 
```c
cube(1 );
```
is the same as 
```c
cube (1);
```
 but 
```c
cub e(1);
```
 will not work as it changes our command name. 
<br><br><br>

## Primitives
There are three different primitive shapes in OpenSCAD we will learn about and primarily use to make our 3D models. They are the cube, which we have already learned about, the sphere, and the cylinder. 
<br><br>

### Cube
Lets review what we learned about the cube command. To create a cube, we use the cube command and give it a parameter for the side lengths. However unlike in geometry class a cube in OpenSCAD can be used to make a rectangular prism. Here is an example:
<br>


```c
cube([5,10,20]);
```

<br>

In this case instead of a side length, we're passing 3 in a vector parameter. A vector parameter in OpenSCAD is designated by the square brackets [], which indicates the dimensions of the cube along the X, Y, and Z axes. By default, one corner of the cube is positioned at the origin, (0,0,0).
<br><br>

#### Understanding Vectors
Imagine you're in a large room, like a gymnasium, and it's completely dark. Now, you're trying to direct a friend to a specific location in that room. Let's say you know the room is 100 steps long, 50 steps wide, and 20 steps high. You can tell your friend to walk forward a certain number of steps, then sideways, and finally climb up a ladder to reach a specific location in the room. This is very similar to how vectors work in OpenSCAD.
<br>
When we talk about a vector in OpenSCAD, like 

```c
[20, 10, 10]
```
, these numbers represent the steps your friend would take in the dark room. The first number, 20, tells them to walk forward 20 steps from where they started (the "origin" point). The second number, 10, means to sidestep 10 steps to the right. The third number, another 10, means to climb a ladder 10 steps upward. 
<br>
So when you're creating a cube in OpenSCAD and write 

```c
cube([20, 10, 10]);
```
, the vector [20, 10, 10] is like instructions for creating a box. It's as if you're saying "make a box that is 20 steps long, 10 steps wide, and 10 steps high".
<br>

In this way, vectors are like instructions for navigating a 3D space, helping the computer to understand where to place things and how big they should be. It's an essential part of building your 3D models.
<br>

#### The Center Parameter 
Now, let's center the cube on the origin. We'll do this using a parameter named 'center'. Remember how we said shape commands in OpenSCAD require a parameter or parameters? We can have multiple parameters and separate them the same way we separate numbers in a vector with a comma. The center parameter is a boolean type parameter. In this context a boolean is a type of parameter that can be true or false. Try it:

```c
cube([10,10,20], center=true);
```

<br><br>

### Sphere 
To create a sphere, we use the sphere command. It takes one measurement, the radius, and places the sphere centered around the origin so it does not need a center  boolean parameter. Here is an example:
<br>

```c
$fn = 40; 
sphere(r=10);
```
<br>

#### Resolution $fn
You may have noticed we started our code with an odd line of text
```c
$fn=40
```
The $fn is a global variable (more on that later, but you can think of it as a parameter for your entire code not just one shape) that controls the number of fragments used to render a circle or sphere - 40 is generally a good choice for this. More fragments yield smoother shapes, but at the cost of more processing time. Try changing the number to 5. 
<br><br>

### Cylinder
Next, let's create a cylinder. We use the cylinder command and we can label parameters like the height (h), the radius at the bottom (r1), and the radius at the top (r2).
<br>


```c
cylinder(h=20, r1=5, r2=5);
```

<br>

Note that cylinders are centered around the Z-axis, and touch the XY plane.
<br><br>

#### Cone
A cone is essentially a cylinder but with different radii at the bottom and top. A pointed cone can be achieved by making r2 equal to 0.
<br>

```c
cylinder(h=20, r1=5, r2=0);
```
<br><br><br>

## Practice Solutions
- Make a top: We'll use two cylinders to make a spinning top. The first cylinder forms the body of the top, while the second cylinder forms the handle.
<br>

```c
cylinder(r1=.3,r2=5,h=4,center=true); 
cylinder(r=.3,h=6); 
```
<br><br>

- Make a stair step: We'll use cubes to make a stair step. Each cube is one step of the staircase. Notice how the X dimension decreases by 1 and the Z dimension increases by 1 for each subsequent cube. This forms the steps of the staircase.
<br>

```c
cube([4,5,1]); 
cube([3,5,2]); 
cube([2,5,3]); 
cube([1,5,4]); 
```
<br><br><br>

## Check for Understanding
After going through this lesson, reflect on the following questions:
<br>

- What are parameters?
- Where are each shape centered?
- How do you make a pointed cone facing down?
<br>

Remember, these are conceptual questions meant to reinforce your understanding of OpenSCAD commands. They do not require actual coding. Answer them to the best of your understanding.
<br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%201/1_1_basic_shapes_student.scad)
- [OpenSCAD terminology](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/terminology.txt)

<br><br>
Happy coding!

<br><br><br>