---
layout: post
title:  "NORwegian Teensy Clip Edition Info"
excerpt: "More info about the NORwegian Teensy Clip Edition board"
info: true
tag:
- NORwegian Teensy Clip Edition
- PS3 Downgrade
comments: false
---
![NTCEGLAMOUR](/assets/img/NTCEGLAMOUR.jpg){:class="img-responsive"}
![NTCETOP](/assets/img/NTCETOP.jpg){:class="img-responsive"}

The NORwegian Teensy Clip Edition is an easy way to read/write to TSOP56 NORs and TSOP48 NANDs using all the various clips out there. You don't need to solder wires between clip daughter boards and the Teensy++ 2.0, just plug the clip directly into the appropriate connector and you're good to go.

It also has a built in 5v to 3.3v voltage regulator, so all you need is a 5v 2Amp USB phone charger in order to power everything.

## Features
* **READ/WRITE NANDS WITH THE E3 NOR CLIP**
* **Read/write NORs with the E3 NOR clip**
* Read/write NANDs with the 360 clip (32 pin)
* Read/write NANDs with the NAND UNI Clip (48 pin)
* Read/write NANDs with the NOR UNI Clip (56 pin)
* Read/write NORs with the NOR UNI Clip (56 pin)
* Can be powered over microUSB with a 2 amp phone charger, no external power supply needed
* Uses an L-C power filter as well as dedicated decoupling capacitors for each clip to provide clean and stable power
* Utilizes the Teensy++ 2.0 in conjunction with judges NORway and NANDway Signal Booster Edition software to read/write NORs and NANDs
* Has 3.3v power output headers

## On The Board:
* 2x E3 connectors one for NANDs, one for NORs
* 2x 60 pin connectors for NOR and NAND UNI clips
* 32 pin connector for 32 pin 360 clips
* MicroUSB power only connector
* Texas Instruments TPS62086 5v to 3.3v 3amp Step-Down converter with L-C filter
* 8x 0.1uF decoupling capacitors
* 2x 10-bit bus switches for switching the circuit between NORway and NANDway Signal Booster Edition
* 4.7k Ohm Resistor for WP (NOR UNI Clip)
* Your choice of either pin headers or a screw terminal block for power output
* Pin header to connect to Tristate (for NORs)

## Requires:
* Teensy++ 2.0
* Any clips you want to use with it
* A computer
* 2 Amp phone charger

Without the Teensy++ 2.0 installed it looks like this.
![NTCETOPMIN](/assets/img/NTCETOPMIN.jpg){:class="img-responsive"}

# Powering the NORwegian Teensy Clip Edition
I recommend using a 5v 2amp USB phone charger with a microUSB cable to power it. But you could power it with an external power supply, just plug it into the 3.3v headers.

The Teensy++ 2.0 can either be powered from the NORwegian Teensy Clip Edition or with a MCP1825 regulator on the Teensy++ 2.0 itself.

If you have a MCP1825 regulator on your Teensy++ 2.0 you shouldn't connect it's 5v pin to the NORwegian Teensy Clip Edition.

If you don't have a regulator on your Teensy++ 2.0 you need to cut the trace between the 5v pad and the 3.3v pad on the bottom of the Teensy++ 2.0 like in the picture.
You then need to make a solder bridge with the 3.3v pad like so. Now when you put the Teensy++ 2.0 on the NORwegian Teensy Clip Edition you can connect the 5v pin.

# Detailed Board Info

You can get the schematics, BOM, and Gerber files on [GitHub](put link here)

NOR uses this pinout

![](https://i.imgur.com/Zx64QzN.gif)

Where possible there is a 0.1uF capacitor connected to pins 29+33 and 43+52. With some of the clips there is only one 0.1uF decoupling capacitor due to their design.

NAND uses this pinout for NANDway SBE (Signal Booster Edition). 

![](https://i.imgur.com/hodHGCp.jpg)

0.1uF capacitors connected to pins 12+13 and 36+37 where possible.

# More Pictures

![NTCETOPBARE](/assets/img/NTCETOPBARE.jpg){:class="img-responsive"}
![NTCEBOTTOMBARE](/assets/img/NTCEBOTTOMBARE.jpg){:class="img-responsive"}