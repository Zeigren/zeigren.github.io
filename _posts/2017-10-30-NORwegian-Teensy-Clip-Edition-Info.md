---
layout: post
title:  "NORwegian Teensy Clip Edition Info"
excerpt: "More info about the board"
tag:
- NORwegian Teensy Clip Edition
- PS3 Downgrade
comments: false
---
![NTCEGLAMOUR](/assets/img/NTCEGLAMOUR.jpg){:class="img-responsive"}
![NTCETOP](/assets/img/NTCETOP.jpg){:class="img-responsive"}

# Powering the NORwegian Teensy Clip Edition
I recommened using a 5v 2amp USB phone charger with a microUSB cable to power it. But you could power it with an external power supply, just plug it into the 3.3v headers.

The Teensy++ 2.0 can either be powered from the NORwegian Teensy Clip Edition or with a MCP1825 regulator on the Teensy++ 2.0 itself.

If you have a MCP1825 regulator on your Teensy++ 2.0 you shouldn't connect it's 5v pin to the NORwegian Teensy Clip Edition.

If you don't have a regulator on your Teensy++ 2.0 you need to cut the trace between the 5v pad and the 3.3v pad on the bottom of the Teensy++ 2.0 like in the picture.
You then need to make a solder bridge with the 3.3v pad like so. Now when you put the Teensy++ 2.0 on the NORwegian Teensy Clip Edition you can connect the 5v pin.

# Detailed Board Info

NOR uses this pinout

![](https://i.imgur.com/Zx64QzN.gif)

Where possible there is a 0.1uF capacitor connected to pins 29+33 and 43+52. With some of the clips there is only one 0.1uF decoupling capacitor due to their design.

NAND uses this pinout for NANDway SBE (Signal Booster Edition). 

![](https://i.imgur.com/hodHGCp.jpg)

0.1uF capacitors connected to pins 12+13 and 36+37 where possible.

# More Pictures

![NTCETOPMIN](/assets/img/NTCETOPMIN.jpg){:class="img-responsive"}
![NTCETOPBARE](/assets/img/NTCETOPBARE.jpg){:class="img-responsive"}
![NTCEBOTTOMBARE](/assets/img/NTCEBOTTOMBARE.jpg){:class="img-responsive"}