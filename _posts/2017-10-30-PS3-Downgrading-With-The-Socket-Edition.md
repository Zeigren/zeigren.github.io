---
layout: post
title:  "PS3 Downgrading With The Socket Edition"
excerpt: "Using the Socket Edition to Downgrade"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- NORwegian Teensy Socket Edition
comments: false
---
# Using the NORwegian Teensy Socket Edition
Since these are sockets and not clips the NAND or NOR has to be desoldered and put into the socket. If you're not super confident in soldering very small things (each pin is only 0.20mm/0.008in thick) this is not the edition for you.

On the Teensy++ 2.0 these pins are not connected to anything on the Socket Edition: B7, ALE, R, GND(pin next to R), +5V, and the three pins for the reset button. 

So you don't need to connect those to the Socket Edition. However I left the holes for all of those on the Socket Edition (except for the three for the reset button), so if you already have pin headers on your Teensy++ 2.0 you don't have to remove them.

On the Teensy++ 2.0 the holes for E4 and E5 are smaller than standard pin header size, so a bit of wire or a smaller pin will need to be used to make a connection to the Socket Edition. I usually use cut off leads from caps or resistors.

In order to insert the NAND or NOR you have to push down on the top of the socket to retract the top pins. Then place the NAND or NOR in with the dot lined up with the 1 on the circuit board.

![Like this](https://i.imgur.com/E8PbUZi.jpg)
Like this





# [If You're Downgrading A NAND Continue to Page 6a]({{ "/PS3-Downgrading-NAND-Dumping-and-Flashing/" | relative_url}})
# [If You're Downgrading A NOR Continue to Page 6b]({{ "/PS3-Downgrading-NOR-Dumping-and-Flashing/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})