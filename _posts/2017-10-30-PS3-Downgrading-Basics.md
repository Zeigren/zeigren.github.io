---
layout: post
title:  "PS3 Downgrading Basics"
excerpt: "What you need to know before you start downgrading"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- Basics
comments: false
---
# PS3 Downgrade Guide Page 1

# What Even Is Downgrading?

Downgrading is taking whatever firmware your PS3 is currently at and in most cases restoring it to firmware 3.55, or downgrading it to CFW(custom firmware).

Once your PS3 is on firmware 3.55 or CFW then you can do all kinds of things. Run homebrew, use Other OS (Linux), etc... None of which you can do if your PS3 is updated past 3.55.

In order to downgrade you have to take apart your PS3 and use some kind of hardware device to write and read the NOR or NAND flash on the motherboard.

Only certain models of PS3s can be downgraded, it doesn't matter what firmware they're at. Just what model they are.

These guides are geared toward using the FlashcatUSB Clip Adapters, NORwegian Teensy Clip Edition and Socket Edition in order to perform downgrades.

# Can I Downgrade?

Check the model number of your PS3 with this chart:
[http://www.psdevwiki.com/ps3/SKU_Models](http://www.psdevwiki.com/ps3/SKU_Models)

If the downgradable min is less than 3.55 then you'll be able to downgrade.

You can also check using [MinVerChk](http://psx-scene.com/forums/content/minverchk-minimum-downgrade-firmware-check-tool-1238/)

* Make a PS3 folder on a flash drive 
* Then make a UPDATE folder inside of that
* Put the PS3UPDAT.PUP inside the update folder
* Plug the flash drive into your PS3
* Go to Settings, System Update, Update via Storage Media
* Click OK
* Then it should tell you then minimum firmware of your PS3

Once you know that you can downgrade, check which type of flash memory your PS3 uses on the same chart. It will either be NOR or NAND. Whether your PS3 is NOR or NAND will determine how you downgrade your PS3. As each is downgraded slightly differently.

The NORwegian Teensy Clip and Socket Edition use a PJRC Teensy++ 2.0 in conjunction with NORway and NANDway in order to perform the downgrade. The FlashcatUSB Clip Adapters are used with the FlashcatUSB xPort from EmbeddedComputers.

PS3 downgrading isn't the easiest thing in the world. I've made this guide and this hardware to try and make it a little easier, but there can still be all kinds of problems and issues you run into along the way.

If you decide that you still want to downgrade your PS3 keep reading the rest of these guides before you even buy anything to do it. That way you know what you're getting into and what you'll need.

# What Steps Are There To Downgrading?

In general this is what downgrading looks like.

* Determine you can downgrade, and if it's NAND or NOR
* Take apart PS3 to remove the motherboard
* Use some hardware flasher to dump the NAND/NOR onto a computer
* Verify that the dump is good
* Patch the dump
* Flash the patched dump back onto the console
* Put your PS3 back together
* Finish doing the software stuff once it's assembled
* Ta-Da downgraded!

# What's All This CFW, OFW, CEX, DEX Nonsense?

So these are all different firmware types that have different features.

OFW is Official/Retail Firmware, the firmware that is made by Sony.

CFW is Custom Firmware, made by people in the PS3 modding community.

CEX are consumer or retail consoles.

DEX are Debug/developer consoles. You can convert a CEX console to a DEX console, if that's what you're into.

REX is the Rebug Custom Firmware for CEX(Consumer)

D-REX is the Rebug Custom Firmware for DEX(Developer)

# [Continue to Page 2 - Getting Started]({{ "/PS3-Downgrading-Getting-Started/" | relative_url}})