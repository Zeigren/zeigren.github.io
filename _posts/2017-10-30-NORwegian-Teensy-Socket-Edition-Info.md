---
layout: post
title:  "NORwegian Teensy Socket Edition Info"
excerpt: "More information about the NORwegian Teensy Socket Edition board itself"
info: true
tag:
- NORwegian Teensy Socket Edition 
- PS3 Downgrade
comments: false
---
![With Teensy++ 2.0 installed](https://i.imgur.com/OxOtkvV.jpg){:class="img-responsive"}

# Board Info

NORwegian Teensy Socket Edition

* TSOP48 ZIF Socket for NANDs
* TSOP56 ZIF Socket for NORs
* 2x 0.1uF decoupling capacitors for each socket (4 in total)
* 4.7k Ohm Resistor for WP (NOR Socket)
* Support for either pin headers or a screw terminal block for external power

Requires:
* Teensy++ 2.0
* External 3.3V DC Power Supply

![](https://i.imgur.com/KIAuCVC.jpg){:class="img-responsive"}

# Powering the NORwegian Teensy Socket Edition

The 5V pin on the Teensy++ 2.0 is not connected to anything on the Socket Edition, so the Teensy++ 2.0 has to be powered over USB. In order to do this the 5v line needs to be cut on the bottom of the Teensy++ 2.0. Then a MCP1825 voltage regulator needs to be soldered to the Teensy++ 2.0 and the 3.3v pad bridged.

## NANDs

When reading and writing to NANDs sometimes an external 3.3V DC power supply isn't necessary.

## NORs

An external 3.3V DC power supply is usually required for reading and writing NORs.

# Detailed Board Info

NOR uses this pinout

![](https://i.imgur.com/Zx64QzN.gif){:class="img-responsive"}

Exception being that there is a 0.1uF capacitor connected to pins 29+33 and 43+52.

NAND uses this pinout for NANDway SBE (Signal Booster Edition). 

![](https://i.imgur.com/hodHGCp.jpg){:class="img-responsive"}

However there is no actual "signal boosting" on this board , there is only one connection each for WE, ALE, CLE, and RE. The signals don't really need to be boosted when there is such a short direct connection between the Teensy++ 2.0 and the NAND. 0.1uF capacitors connected to pins 12+13 and 36+37.

# Photos

![Bare Board Top](https://i.imgur.com/JpjX1oX.jpg){:class="img-responsive"}
Bare Board Top

![Top With Sockets and Teensy++ 2.0](https://i.imgur.com/Y73uqSJ.jpg){:class="img-responsive"}
Top With Sockets and Teensy++ 2.0

![Bottom with Sockets Installed](https://i.imgur.com/MdSOWkf.jpg){:class="img-responsive"}
Bottom with Sockets Installed