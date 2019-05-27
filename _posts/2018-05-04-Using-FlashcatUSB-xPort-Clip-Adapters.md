---
layout: post
title:  "Using FlashcatUSB Clip Adapters"
excerpt: "A basic guide to using the FlashcatUSB Clip Adapters"
fcadaptersguide: true
tag:
- Guide
- FlashcatUSB
- xPort
- Resources
comments: false
redirect_to: https://docs.zeigren.com/books/flashcatusb-clip-adapters
---

[Here](https://youtu.be/0JLvI2vaAI8) is a video I made about the clip adapters as well as a basic tutorial on using them with the FlashcatUSB xPort. I've made a more in depth [tutorial video](https://youtu.be/mcuzO3ZSaBg) and a video going over some [troubleshooting](https://youtu.be/43VDcZQesHo) steps.

Here's some other useful info though.

---

## PS3 NAND Dumping

When you are dumping the NAND from a PS3 there is one setting that you need to change.

Under Mode > Protocol Settings
![Protocol Settings](/assets/img/FlashcatAdapters/Protocol Settings.png){:class="img-responsive"}

At the bottom you need to change the main/spare area layout to combined.
![NAND Combined](/assets/img/FlashcatAdapters/NAND Combined.png){:class="img-responsive"}

Otherwise the NANDs won't work correctly with all the regular PS3 tools.

You can first dump the NAND then use the comparison tool built into the software to make sure that you got a good dump.

---

## PS3 NOR Dumping

Since the FlashcatUSB xPort doesn't have a pin for setting the Tristate, you need to solder a wire from the Tristate to a GND point. This can either be to one of the GND pins on the clip adapter itself, or to a GND point on the PS3.

You can first dump the NOR then use the comparison tool built into the software to make sure that you got a good dump.

---

Have any questions or just want to talk about the FlashcatUSB xPort Clip Adapters? Head on over to the [Riot.im](https://riot.im) room at [#FCXAdapters:matrix.org](https://riot.im/app/#/room/#FCXAdapters:matrix.org). You can also visit the [BlackCatUSB](https://www.blackcatusb.net/index.php) forum where there's already a [thread](https://www.blackcatusb.net/index.php?threads/tsop56-48-nor-nand-clip-adapters-for-the-flashcatusb-xport.493/) for the adapters. Or you can of course e-mail me or leave a comment on the forum thread of your choice.
