---
layout: post
title:  "Libraries: External Libraries in OpenSCAD"
date:   1111-04-01
last_modified_at: 2023-06-29
categories: [OpenSCAD]
tags: [Bonus]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

## Learning Objectives
By the end of this lesson, students should be able to:
1. Understand what libraries are and their importance in OpenSCAD.
2. Know how to include libraries in their projects.
3. Be able to use built-in libraries such as the MCAD library.
4. Install and utilize external libraries.

<br><br>

## Exploring Libraries in OpenSCAD
Libraries in OpenSCAD, like in many other programming environments, are repositories of prewritten code that can be used to enhance your projects. They can significantly boost your productivity by providing functions and modules that you don't have to write yourself.

In this lesson, we're going to explore how to use libraries with OpenSCAD, particularly the built-in MCAD library. Check out the different regular shapes you can create with just a few lines of code:
```OpenSCAD
use <MCAD/regular_shapes.scad>
cylinder_tube(20, 10, 1);
triangle_prism(20,10);
```

<br><br><br>

## Practical Application of Libraries
Libraries can come with constants and predefined measurements, which makes designing parts easier. For instance, the `units.scad` file from the MCAD library provides measurements for bolts. Here is an example of how to create a M3 bolt with the correct dimensions:

```OpenSCAD
use <MCAD/nuts_and_bolts.scad>
include <MCAD/units.scad>
$fn=50;
//M3 is an alias for 3. It is defined in units.scad
translate([14, 0, 0]){
    boltHole(M3, length=10);
    rotate([180,0,0])
    nutHole(M3, tolerance=0.0);
}
```

<br><br><br>

## Installing and Using Libraries
While OpenSCAD comes with some built-in libraries, most will need to be downloaded and installed. This process typically involves downloading the library's code, unzipping the file if necessary, and placing the folder with the code into the library directory.

Once a library is installed correctly, you can call its code as if it were built-in:

```OpenSCAD
use <name_of_library/library_file.scad>
// Code using the library
```

<br><br><br>

## Review
In this lesson, you learned:
- The importance of libraries in OpenSCAD.
- How to include and use the built-in MCAD library.
- How to install and utilize external libraries.
- How libraries can make your 3D design process more efficient.

<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%202/2_2_bool_diff_student.scad)
- [MCAD Library](https://github.com/openscad/MCAD)
- [OpenSCAD Libraries](https://openscad.org/libraries.html)
- [OpenSCAD Libraries Documentation](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/Libraries)
<br><br><br>