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
---

I have made a short [video](https://youtu.be/0JLvI2vaAI8) about the clip adapters and using them that you can check out.

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

Have any questions or just want to talk about the FlashcatUSB xPort Adapters? Head on over to the [Riot.im](https://riot.im) room at [#FCXAdapters:matrix.org](https://riot.im/app/#/room/#FCXAdapters:matrix.org). Or you can of course e-mail me or leave a comment on the forum thread of your choice.