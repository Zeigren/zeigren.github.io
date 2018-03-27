---
layout: post
title:  "PS3 Downgrading Setting Up The Socket Edition"
excerpt: "Setting up the hardware and software for the Socket Edition"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- Setting Up
- NORwegian Teensy Socket Edition
comments: false
---
# Hardware
## Socket Edition
### Teensy++ 2.0

First things first the Teensy++ 2.0 needs some attention before soldering it to the Clip Edition. 
In order for it to work correctly the trace between the 5v and 3v on the bottom of the Teensy++ 2.0 needs to be cut.

![Teensy5vcut Before](/assets/img/Teensy5vcutBefore.png){:class="img-responsive"}
![Teensy5vcut After](/assets/img/Teensy5vcutAfter.png){:class="img-responsive"}
(images from psdevwiki.com)

Then the 3v pads need to be bridged with solder and a MCP1825 regulator needs to be soldered on as well. Like this
![3Vsolder](/assets/img/3vsolder.png){:class="img-responsive"}
(image from psdevwiki.com)

Now the Teensy++ 2.0 is ready to be soldered to the Socket Edition.

I recommend placing the pins into the Socket Edition, then place the Teensy++ 2.0 on top of the pins,
solder the pins to the Teensy++ 2.0, then flip the whole thing over and solder the pins to the Socket Edition.

If you solder the pins to the Teensy++ 2.0 first then try putting it into the Socket Edition you'll probably have to bend some of the pins into place.

You don't need to solder a pin to ALE on the Teensy++ 2.0.

### E4 and E5

The holes on the Teensy++ 2.0 for E4 and E5 and much smaller than your regular header pin. You need a pin that is about 0.6mm in diameter.
This what one of the jumper wires is for!

The pins on the ends of the jumper wires are small enough to be used to connect E4 and E5 on the Teensy++ 2.0 to the Socket Edition.

Just take a jumper wire, cut off the pins on each end. 
Put it through the hole on the Teensy++ 2.0 and into the corresponding hole on the Socket Edition and solder them in place.

You don't need to use the pin from a jumper wire, any other small pin like thing will work or tiny wires.

### Power

Teensy++ 2.0 is powered by onboard regulator. The Socket Edition needs an external 3.3v power supply.

# Software

If you downloaded my PS3 Downgrading Files.zip, just extract that you'll be good to go. You can skip this part.

If you didn't you should make a dedicated folder for all the PS3 downgrading stuff, that way it's easy to find when you need it.

I recommend using WAY-launchers GUI by littlebalup https://github.com/littlebalup/WAY-launchers

You can reprogram your Teensy++ 2.0 using it and it makes it easy to use NORway and NANDway.
No inputting commands just clicking buttons.

You'll need to download and install python 2.7.2, pyserial 2.5, and the Teensy++ 2.0 drivers.

Then download NORway and NANDway by judges.
You need NORWay.hex, NORway.py, NANDway.py, and NANDway_Signal_Booster_Edition.hex.
Then put those all in the same folder as WAY-launchers.exe.


I would recommend making a folder for your raw dumps, and another folder to copy them into. Then anything you do will be to the copies.
That way your original dumps don't get messed up if you need them later.


You will also want PS3DumpChecker and other checkers. To check your NAND/NOR.


FlowRebuilder to put NANDs together.


The FSM files. OFW and CFW stuff. Whatever other stuff you need.

Here's what my folder looks like.

# [Continue to Page 5b - Downgrading With The Socket Edition]({{ "/PS3-Downgrading-With-The-Socket-Edition/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})