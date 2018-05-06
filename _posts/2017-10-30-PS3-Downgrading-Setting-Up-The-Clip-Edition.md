---
layout: post
title:  "PS3 Downgrading Setting Up The Clip Edition"
excerpt: "Setting up the hardware and software for the Clip Edition"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- Setting Up
- NORwegian Teensy Clip Edition
comments: false
---
# Hardware
## Clip Edition
For this next part I'm going to assume that you have a brand new Teensy. 

If you don't have a brand new Teensy and have used it for downgrading before and it has a regulator installed check the power section for power options.

### Soldering
There isn't much soldering you have to do with the Clip Edition, 
if you have me install the Teensy++ 2.0 on it for you then you might not need to solder anything at all!

#### Teensy++ 2.0
First things first the Teensy++ 2.0 needs some attention before soldering it to the Clip Edition. 
In order for it to work correctly the trace between the 5v and 3v on the bottom of the Teensy++ 2.0 needs to be cut. Be careful to just cut through the exposed trace, you don't want to cut too deep and cut into the board.

![Teensy5vcut Before](/assets/img/Teensy5vcutBefore.png){:class="img-responsive"}
![Teensy5vcut After](/assets/img/Teensy5vcutAfter.png){:class="img-responsive"}
(images from psdevwiki.com)

Then the 3v pads need to be bridged with solder. Like this
![3vBridged](/assets/img/3vBridged.jpg){:class="img-responsive"}


To double check that the 5v trace is cut, use a multimeter and put it into continuity mode. The mode where it beeps if you put the probes together lol. Then put one probe on the 5v pad on bottom, and one in the 5v hole. If it beeps then the trace wasn't cut all the way. Also do the same thing but with the 3v pads you just soldered and the 5v hole, if it beeps then your solder joint is good!

![3vBridgedCheck](/assets/img/3vBridgedCheck.jpg){:class="img-responsive"}
Now the Teensy++ 2.0 is ready to be soldered to the Clip Edition.

I recommend placing the pin headers into the Clip Edition, then place the Teensy++ 2.0 on top of the headers
![NTCEHEADERS](/assets/img/NTCEHEADERS.jpg){:class="img-responsive"}
Then solder the headers to the Teensy++ 2.0, then flip the whole thing over and solder the headers to the Clip Edition. You'll want headers for everything except, ALE, E4 and E5 (E4 and E5 covered below).

If you solder the pins to the Teensy++ 2.0 first then try putting it into the Clip Edition you'll probably have to bend some of the pins into place.


#### E4 and E5
The holes on the Teensy++ 2.0 for E4 and E5 and much smaller than your regular header pin. You need a pin that is about 0.6mm in diameter.
This what one of the jumper wires is for!

The pins on the ends of the jumper wires are small enough to be used to connect E4 and E5 on the Teensy++ 2.0 to the Clip Edition.

Just take a jumper wire, cut off the pins on each end. 
Put it through the hole on the Teensy++ 2.0 and into the corresponding hole on the Clip Edition and solder them in place.

You don't need to use the pin from a jumper wire, any other small pin like thing will work or tiny wires.

#### Tristate on NOR consoles
If your console is a NAND console you can skip this. If it's a NOR you'll need it.

For NOR consoles you have to solder a wire from Tristate on the clip edition to Tristate on the PS3 motherboard. Here are some pictures of the Tristate locations for different boards. Images from psdevwiki.com.

#### DIA-001/DIA-002
![DIA-001_BOTTOM](/assets/img/DIA-001_BOTTOM.jpg){:class="img-responsive"}
![DIA-001_NOR](/assets/img/DIA-001_NOR.jpg){:class="img-responsive"}

#### VER-001
![VER-001_BOTTOM](/assets/img/VER-001_BOTTOM.jpg){:class="img-responsive"}
![VER-001_NOR](/assets/img/VER-001_NOR.jpg){:class="img-responsive"}

#### DYN-001
![DYN-001_BOTTOM](/assets/img/DYN-001_BOTTOM.jpg){:class="img-responsive"}
![DYN-001_NOR](/assets/img/DYN-001_NOR.jpg){:class="img-responsive"}

#### SUR-001/JTP-001/JSD-001
![JTP-001_BOTTOM](/assets/img/JTP-001_BOTTOM.jpg){:class="img-responsive"}
![JSD-001_NOR](/assets/img/JSD-001_NOR.png){:class="img-responsive"}


I recommend soldering a wire to Tristate on the PS3 and taping it down, then only connect it to the Clip Edition once you have everything else set up and your clip in place.
![TRISTATE](/assets/img/TRISTATE.jpg){:class="img-responsive"}

### Power
Use a 5v 2 Amp USB charger of some kind and a micro USB cable and plug it into the Clip Edition. 
You won't get enough power from plugging it into a USB port on your computer. Many Android phones use 5v 2 Amp USB chargers so they're easy to come by.
Your charger may say 2000ma instead, that's the same as 2 Amps. You can use chargers that are over 2 Amps, just 2 Amps is the recommended minimum.
![CHARGER](/assets/img/CHARGER.jpg){:class="img-responsive"}

If you have a Teensy++ 2.0 that already has a voltage regulator on it you can either remove it, or don't connect the 5v pin on the Teensy++ 2.0 to the Clip Edition.



# Software
If you downloaded my PS3 Downgrading Files.zip, just extract that and you'll be good to go. You can skip this part.

If you didn't you should make a dedicated folder for all the PS3 downgrading stuff, that way it's easy to find when you need it.

I recommend using [WAY-launchers GUI by littlebalup](https://github.com/littlebalup/WAY-launchers)

You can reprogram your Teensy++ 2.0 using it and it makes it easy to use NORway and NANDway. 
No inputting commands just clicking buttons.

You'll need to download and install python 2.7.2, pyserial 2.5, and the Teensy++ 2.0 drivers.

Then download NORway and NANDway by judges.
You need NORWay.hex, NORway.py, NANDway.py, and NANDway_SignalBoosterEdition.hex. 
Then put those all in the same folder as WAY-launchers.exe.


I would recommend making a folder for your raw dumps, and another folder to copy them into. Then anything you do will be to the copies.
That way your original dumps don't get messed up if you need them later.


You will also want PS3DumpChecker and other checkers. To check your NAND/NOR.


FlowRebuilder to put NANDs together.


The FSM files. OFW and CFW stuff. Whatever other stuff you need.

Here's what my folder looks like.
![PS3FOLDER](/assets/img/PS3FOLDER.PNG){:class="img-responsive"}


# [Continue to Page 5a - Downgrading With The Clip Edition]({{ "/PS3-Downgrading-With-The-Clip-Edition/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})