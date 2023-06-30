---
layout: post
title:  "Coding Fundamentals: Debugging and Fixing Syntax Errors"
date:   1111-01-05
last_modified_at: 2023-06-28
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
At the end of this lesson, you will be able to:
1. Understand what debugging is and why it's necessary.
2. Identify different windows in OpenSCAD.
3. Find and fix syntax errors in your code.
<br><br><br>

## Understanding Debugging
Debugging is the process of fixing errors in your code. In this lesson, we'll focus on syntax errors, which occur when you type something incorrectly. Syntax errors are typically straightforward to fix. Debugging can also involve correcting code that is not behaving as expected, such as code intended to cut a cube in half but instead makes the cube larger.
<br><br><br>

## Different Windows in OpenSCAD
OpenSCAD has several distinct windows:
- **Editor**: Where you type your code.
- **Console**: Outputs from renders and previews. Contains a mix of important and less crucial text.
- **Error-Log**: Displays a table of the errors in your code, generally appearing one at a time.
- **Customizer**: Not necessary for this lesson.
- **Model Preview**: Provides a preview of the model when rendered.

You can navigate between windows by pressing Alt+W and selecting the desired window.
<br><br><br>

## Finding and Fixing Errors
Follow these steps to find and fix errors in your OpenSCAD code:
1. Preview code (F5).
2. Use Ctrl+Alt+E to jump to an error.
3. Arrow through your code to understand the error, possibly missing punctuation.
4. If needed, navigate to the error-log window (Alt+W+L) for more details.
5. If the error remains elusive, begin at the top of the code and review each line. 

Remember to ensure punctuation is being read aloud by your screen reader.
<br><br><br>

## Practice Problems
Try to fix the following lines of code and then comment them out:
1.
```c
cyliner(4,4,4)
```
2.
```c
sphere[r=1
```
3.
```c
tranlate[0,0,1]
sphere(1);
```
<br><br>

### Practice Solutions
1. 
```c
cylinder(4,4,4);
```
2. 
```c
sphere(r=1);
```
3. 
```c
translate([0,0,1])
sphere(1);
```
<br><br><br>

## Review
In this lesson you learned:
- The concept of debugging in coding and its importance.
- How to navigate between different windows in OpenSCAD.
- Steps to find and fix syntax errors in your code.
<br><br><br>

## Resources
- [Follow along code](https://raw.githubusercontent.com/funkonaut/openSCAD_lessons/main/Lessons/Lesson%202/2_2_bool_diff_student.scad)
<br><br><br>