---
layout: post
title:  "PS3 Downgrading Getting Started"
excerpt: "The hardware and software you'll need to downgrade"
guide: true
tag:
- Guide
- PS3 Downgrade
comments: false
---
# Getting Started
Please read the entire guide before you actually start (**all of it**, yes I know it's long). 
That way you know what you're getting into and what things you might need for your particular setup.

I'm also in **NO WAY** responsible for you messing up or destroying anything in the process of downgrading. 
I and many others have tried to make this as easy and foolproof as possible, but things can go wrong, freak accidents happen, and not everyone is the brightest tool in the shed.


# Hardware
## Clip Edition
![NTCEGLAMOUR](/assets/img/NTCEGLAMOUR.jpg){:class="img-responsive"}
You will need
* A NORwegian Teensy Clip Edition
* A Teensy++ 2.0
* A 5v 2Amp USB power adapter (USB phone charger)
* A microUSB cable to power the NORwegian Teensy Clip Edition
* A miniUSB cable to connect the Teensy++ 2.0 to your computer
* Whatever clip you would like to use
* 48x 2.54mm Pin Headers (if you don't have them on your Teensy++ 2.0 already)
  * [These would work](https://www.amazon.com/Hotop-Pack-Single-Header-Connector/dp/B06XR8CV8P/ref=sr_1_8?ie=UTF8&qid=1509273572&sr=8-8&keywords=pin+header), just break them apart into what you need
* Jumper Wires (2x for connection to the Teensy++ 2.0, 1x for Tristate on NOR consoles)
  * [Like these](https://www.amazon.com/Solderless-Flexible-Breadboard-Jumper-100pcs/dp/B005TZJ0AM/ref=sr_1_4?s=electronics&ie=UTF8&qid=1509248805&sr=1-4&keywords=jumper+wires) 
* A soldering iron (If you're doing NANDs and have me put the Teensy++ 2.0 on for you, you don't need to solder at all!)
* Solder
* Flux
* Thermal Paste
* Screwdrivers 
* Paper towels, Q-Tips
* Isopropyl Alcohol
* A multimeter, any cheap one will do

### All The Clips
As you know the Clip Edition supports every clip, at least every clip I know of. It also lets you use some of the clips in ways they were not designed.

But which clip is right for you?

#### E3 Flasher Clip / E3 Flasher NOR Clip Suit
![E3CLIP](/assets/img/E3CLIP.jpg){:class="img-responsive"}
You can use it for both **NORs** and **NANDs** on the Clip Edition. 

The E3 clip is relatively cheap and easy to come by. It has a pretty long cable and depending on the version of the clip you get you might not need to trim it in any way, you'll have to trim it for use with a NAND though.

You do have to twist the cable around to actually use it, 
and since it is such a long thin cable the wires in the cable are smaller than some of the other clips.
So it might not be as good as some of the other clips.

The Clip Edition makes it possible to use the E3 clip for NAND downgrading, but it is **annoying** to say the least. It can be quite fiddly, but it is doable.

#### NOR UNI Clip (56 pin)
![56UNICLIP](/assets/img/56UNICLIP.jpg){:class="img-responsive"}
It can be used for both NOR and NAND consoles.

These are more expensive then the E3 clip, and are harder to come by.

It has a shorter, thicker cable. So you might have better luck using it over the E3 if you're having problems.

Probably just as fiddly to use for NANDs as the E3 clip.

#### NAND UNI Clip (48 pin)
![48UNITOP](/assets/img/48UNITOP.jpg){:class="img-responsive"}
Just for NAND consoles.

About the same price as the NOR UNI Clip, with the same cable. Isn't super easy to come by.

Easier to use for NANDs, since it's made to do that.
#### NAND 360 Clip (32 pin)
![360TOP](/assets/img/360TOP.jpg){:class="img-responsive"}
The OG NAND clip. Just for NAND consoles.

These aren't as plentiful as they once were.
Pretty much as good as the NAND UNI Clip.

## Socket Edition
![NORwegianTeensySocketEdition](/assets/img/NORwegianTeensySocketGlamour.jpg){:class="img-responsive"}
* A NORwegian Teensy Socket Edition
* A Teensy++ 2.0
* A External 3.3v power supply
* Whatever soldering/hot air stuff you have to use to remove the NOR/NAND

# Software
To make it easy I made a zip file with the exact folder structure I use, and with all the files you need inside of it.

You can [download it here](https://mega.nz/#!ovIEhS5D!Eke5679s1qnOJEv8Bs3BSBIGjsHzn5Zzmj0-w6hrAk4)

This is where I got all those programs, so you can check there for updates in the future and if you want to download all the files yourself.

* [NORway/NANDway by judges](https://github.com/hjudges/NORway)
* [WAY-launchers GUI by littlebalup](https://github.com/littlebalup/WAY-launchers) 
* [Teensy++ 2.0 Serial Driver](https://www.pjrc.com/teensy/usb_serial.html)
* [Teensy Loader](https://www.pjrc.com/teensy/loader_win10.html)
* [Pyserial 2.5](https://pypi.python.org/pypi/pyserial/2.5)
* [Python 2.7.2](https://www.python.org/download/releases/2.7.2/)
* [PS3DumpChecker](https://github.com/Swizzy/PS3DumpChecker)
* [FlowRebuilder 5.2](http://www.ps3hax.net/showthread.php?t=95794)
* [BwE Validator](http://psx-scene.com/forums/content/bwe-nor-validator-v1-30-3373/)
* [Other Files I Just Took from Bailey's Guide](http://www.ps3hax.net/showthread.php?t=39766)
I'll try to fill in the sources of those files later.

# [Continue to Page 3 - PS3 Teardown]({{ "/PS3-Downgrading-PS3-Teardown/" | relative_url}})