---
layout: post
title:  "Using Import, Scale and Size Commands in OpenSCAD"
date:   1111-02-01
last_modified_at: 2023-06-16
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
By the end of this lesson, you will be able to:
- Understand the function and use of the import, scale and size commands in OpenSCAD.
- Import a 3D model using the import command.
- Adjust the size and proportions of 3D models using scale and size commands.
- Combine these commands to modify and control 3D models effectively.

## Using the Import Command in OpenSCAD
The import command is your magic doorway to bring in external 3D models into OpenSCAD. This could be anything, from a basic shape you want to modify, to a complex model you want to incorporate into your design. To import a file, you simply need to specify the file path in the import command like so: `import("file_path");`. Remember, the file path is like the address of your 3D model in your computer.

## Scaling and Sizing 3D Models
Sometimes, the imported model is too big or too small for our needs. That's where the scale and size commands come in. These commands allow you to adjust the size of your 3D models.

- **Scale Command:** The scale command changes the size of a model by a certain factor. For example, `scale([2,2,2])` will double the size of your model in all dimensions. You can also scale your model differently in each dimension. For instance, `scale([1,2,1])` will keep the model's size in the X and Z directions, but double it in the Y direction.

- **Size Command:** The size command sets the size of your model to a specific value. For example, `resize([10,10,10])` will set your model's size to 10 units in all dimensions. Just like the scale command, you can set the size differently in each dimension.

## Review
In this lesson you learned:
- How to use the import command to bring external 3D models into OpenSCAD.
- How to use the scale command to adjust the size of your 3D models by a certain factor.
- How to use the size command to set the size of your models to specific values.

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%201/1_4_import_scale_size_student)
- [OpenSCAD User Manual](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/The_OpenSCAD_Language)
<br><br><br>