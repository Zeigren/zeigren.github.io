---
layout: post
title:  "Hedgehog1286 Expansions Info"
excerpt: "More information about the Hedgehog1286 Expansions"
info: true
tag:
- Hedgehog1286
- Expansions
comments: false
---
![With Teensy++ 2.0 installed](https://i.imgur.com/OxOtkvV.jpg)

Currently for sale on the AssemblerGames Marketplace
https://www.assemblergames.com/threads/norwegian-teensy-nand-nor-reader-writer-ps3-downgrading.67027/

# Board Info
NORwegian Teensy Socket Edition


Comes installed with:
* TSOP48 ZIF Socket for NANDs
* TSOP56 ZIF Socket for NORs
* 2x 0.1uF decoupling capacitors for each socket (4 in total)
* 4.7k Ohm Resistor for WP (NOR Socket)
* Your choice of either pin headers or a screw terminal block for external power

Requires:
* Teensy++ 2.0
* External 3.3V DC Power Supply

![](https://i.imgur.com/KIAuCVC.jpg)



# Powering the NORwegian Teensy Socket Edition
The 5V pin on the Teensy++ 2.0 is not connected to anything on the Socket Edition, so the Teensy++ 2.0 has to be powered over USB. In order to do this the 5v line needs to be cut on the bottom of the Teensy++ 2.0. Then a MCP1825 voltage regulator needs to be soldered to the Teensy++ 2.0 and the 3.3v pad bridged.

## NANDs
When reading and writing to NANDs often times an external 3.3V DC power supply isn't necessary.

## NORs
An external 3.3V DC power supply is required for reading and writing NORs.

# Detailed Board Info

NOR uses this pinout

![](https://i.imgur.com/Zx64QzN.gif)

Exception being that there is a 0.1uF capacitor connected to pins 29+33 and 43+52.

NAND uses this pinout for NANDway SBE (Signal Booster Edition). 

![](https://i.imgur.com/hodHGCp.jpg)

However there is no actual "signal boosting" on this board , there is only one connection each for WE, ALE, CLE, and RE. The signals don't really need to be boosted when there is such a short direct connection between the Teensy++ 2.0 and the NAND. 0.1uF capacitors connected to pins 12+13 and 36+37.

# Photos
![Bare Board Top](https://i.imgur.com/JpjX1oX.jpg)
Bare Board Top

![Top With Sockets and Teensy++ 2.0](https://i.imgur.com/Y73uqSJ.jpg)
Top With Sockets and Teensy++ 2.0

![Bottom with Sockets Installed](https://i.imgur.com/MdSOWkf.jpg)
Bottom with Sockets Installed