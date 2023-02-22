---
layout: post
title:  "Fab Lab Laser Cutting: Using the Glowforge App for BVI Makers (Part 1)"
date:   1113-02-02
last_modified_at: 2023-01-24
categories: [Fabrication Lab]
tags: [Laser Cutting]
---
<br>

## Contents
{:.no_toc}
* Table of contents
{:toc}
<br><br>

## Learning Objectives
In this lesson you will learn how to navigate the Glowforge application with a screen reader by cutting out a simple key chain design from a repository of pre-made designs. Currently there are some accessibility limitations to laying out and uploading your design in the web application. We are working with Glowforge to improve work flow and resolve the issues for screen reader users, but in the meantime we recommend laying out your designs in OpenSCAD or another accessible layout application that works with vector and raster files, and then uploading the whole design into openSCAD. In part two of this lesson we will dive deeper into the web application and go over adjusting settings and other aligning multiple objects. **IMPORTANT NOTE: This step by step is simply for using the Glowforge web app with a screen reader it does not cover very important safety instructions for using hte laser cutter, please complete a safety training before making any cuts**
<br><br><br>

## Materials and Tools
- A (preferably new) 11" by 19.5" sheet of [proofgrade material](https://shop.glowforge.com/collections/materials)
- Glowforge laser cutter
- Computer with an internet connection
- A screen reading software
- An accessible measuring device
<br><br><br>

## Step by Step Instructions
The following sub sections will go over your first laser cut. Before you begin download one of the key chain design files from this [google folder](https://drive.google.com/drive/u/0/folders/1m3VweN7iyKRvgXnwPwTxe4nmGAdFkEvE) they are all two by two inches to begin. This lesson is only on using the Glowforge web app if you are interested in designing for the Glowforge laser cutter check out our lessons on laser cutter design and OpenSCAD Lesson 4. 
<br><br>


### Creating a New Design
Once logged in to the [Glowforge web app](https://app.glowforge.com/) (your laser cutter administrator should be able to supply you with login information or a computer that is already logged into the web app). You will need to create a new Design from the home page. *Note: the following instructions may change periodically as Glowforge changes their web app*
<br><br>

1. Activate the "Create a new design" form field button
2. Activate the "Create a blank design" link menu item
3. You are now in the Glowforge web app design space it won't have an audio indicator but you can tab and you will here you are in a list with multiple items this is the top web page menu bar.
<br><br>

### Uploading a Design 
Now that you are in the Glowforge web app design space you will upload your design to the web app to upload it to the laser cutter.
<br><br>
1. Activate the "Import artwork" form field button
2. Activate the "Upload" form field button 
3. Select the key chain file you downloaded in the pop up file dialogue 
<br><br>

### Resizing and Positioning Your Design
All of the designs in the google folder will default to the top left portion of the Glowforge bed. Depending on if you have used material you may need to reposition the design. We recommend keeping tactile calipers or an accessible measuring tool around to help you figure out where you need to place your design on in the web app. 
<br><br>

#### Resizing your Design *(Optional)*
If you would like your key chain to be smaller or larger then 2" by 2" you can resize it with the following steps. Your design should be focused and selected if you are having trouble finding elements in the steps below try hitting escape a couple of times and then making sure the Virtual PC cursor is off (forms mode) and then select all by pressing control + a.
<br><br>

1. With your design selected activate the "Reposition and resize artwork" form field button
2. Activate the W form field to resize the width of your key chain. 
3. Type out the value in inches you would like to make your key chain.
4. Changing the value of your designs with will automatically scale the design's height (H form field). 
<br><br>

#### Determining Placement for Used Materials *(Optional)*
If you are using used materials (they have holes in them from others laser cuts) then you will want to make sure you place your design where there is un modified material. If you are using a fresh sheet of 11" by 19.5" material you can skip this.
<br><br>

1. Grab your accessible measuring device and your laser cutter materials on a surface square up the material so you know where the top left corner is 
2. Determine a place where you will have enough square inches to cut out your design. Give your self some room for error. So if your design is 2" by 2" find a blank space that is roughly 3" by 3"
3. Measuring parallel to the X and Y axis note the approximate distances (you will have two measurements) from the top left corner to your blank space in inches.
4. You will use these X and Y measurements to position your design in the Glowforge web app. Measurements are made from the top left corner of the material sheet (see "Making the Cut" section for more detail on sheet placement in the machine) and the top left corner of your object. A positive X value is to the right and a positive Y value is down from the left corner.
5. In the "Reposition and resize artwork" form field button (see above steps under the "Resizing your Design" heading). Activate the X form field to type in your X distance in inches and then the Y form field to type in your Y distance in inches.
<br><br>

### Making the Cut
Now that your design is ready lets make the cut (and engrave...). We will first upload our design to the Glowforge then load in our materials and then finally fire the laser. Before completing these steps make sure your laser system is ready to go (ie bed is clear, exhaust system is on, etc.)
<br><br>

#### Loading the Material
1.  Make sure the QR code on your material is face up (there is a large sticker that you will be able to feel where the QR code is). This QR code will tell the Glowforge what material settings to cut and engrave your design with.
2. Open the top and bottom lids of the Glowforge 
3. Load up a sheet of material if you are using an 11" by 19.5" sheet of material make sure it fits flush with the smooth side rails on the honey comb print bed and is pushed up against the bottom door of the Glowforge.
4. Close the bottom and then the top lids. Make sure you close the bottom lid fully or the top lid will not close and the Glowforge will not work.
<br><br>

#### Confirm Material Settings
You will want to double check your material settings incase your QR code was damaged. After the machine scans your material into the Glowforge it will show up in the design space after about 30 or so seconds. You will now see a new form field button something like "Medium Blue Acrylic" or whatever your material is if you do not you will see an "UNKNOWN" form field button. If that is the case activate the button and type the material you want in the search bar then tab through the results until you hear the material you are using and activate it.
<br><br>

#### Setting Engrave Settings *(Optional)*
You will most likely want to change the engrave settings so the graphic design is a bit more pronounced. The default setting is "Draft Graphic" with is acceptable but leaves wanting more... Unfortunately this is a little bit cumbersome due to the web apps somewhat inaccessible design, but it is doable.
<br><br>

1. Focus (but do not activate) the "Print" form field button
2. Tab or arrow key to "Clickable draggle item dot..." this should be the engrave graphic
3. Your virtual PC cursor will need to be on, in browse mode press enter on the above focus element
4. There should now be some new form field buttons on screen. We suggest activating the "3D Engrave" or "SD Graphic" form field buttons. The 3D Engrave setting is deeper while the SD Graphic setting provides a nice frosting effect especially on translucent material.
<br><br>

### Firing the Laser
1. Activate the "PRINT" form field button. *Note: If this is your machines first cut there may be some link that you have click on like "blah blah first cut blah blah" click that or your design won't upload to the machine.*
2. It will take around 30 seconds to a minute for your design to process and upload to the machine if you are interested there is a cancel link that shows up (for canceling the print) above that link is some text that will give you a seconds and minutes read out for how long your design is going to take to make it should be around 5 to 10 minutes depending on the size of your key chain.
3. Go to the laser cutter make sure the exhaust system is on and put on laser safety glasses. There is a large (~3" in diameter) button that should be flashing blue. If you hit it it will start firing the laser. If you hit it again it will pause the laser. If at any time you open the lid while the laser is firing the machine will cancel your print.
4. Hit the fire laser button! The machine should start making a lot of noise (the internal fan will switch on and the motors will move the laser head). Stick around and make sure the smell never gets more then a campfire smell, its a good idea to have a sighted laser cutter admin with you for your first cuts or if you ever are cutting non proof grade material. 
5. When the machine is done cutting it will go through a short cool down sequence that last around 30 seconds. I like to wait an additional 45 seconds to a minute to let the fan clear out any remaining fumes. 
Open the lid and remove your material and print. Scan the crumb tray and make sure your print has been removed. If you have any pieces that are waste you can use a shop vacuum below the machine to remove them or pick them out of the machine.
6. You will now need to clean the masking tape material off of your print. I recommend using a super tacky tape to pull the less tacky masking tape off of your print. 
7. When your print is clean you can now enjoy your new key chain. CONGRATS ON YOUR NEW OBJECT!
<br><br><br>

## Review
In this lesson you learned:
- How to create a design in the Glowforge web app
- How to upload a design to the Glowforge web app
- How to reposition and resize a design in the Glowforge web app
- How to load material into and remove material from the Glowforge 
<br><br><br>

## Resources
- [Glowforge web app](https://app.glowforge.com/) 
- [Key chain design repo (Google Drive folder)](https://drive.google.com/drive/u/0/folders/1m3VweN7iyKRvgXnwPwTxe4nmGAdFkEvE) 
<br><br><br>