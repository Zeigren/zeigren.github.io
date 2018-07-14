---
layout: post
title:  "PS3 Downgrading Setting Up The FlashcatUSB Clip Adapters"
excerpt: "Setting up the hardware and software for the FlashcatUSB Clip Adapters"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- Setting Up
- FlashcatUSB Clip Adapters
comments: false
---

I have a [tutorial video](https://youtu.be/mcuzO3ZSaBg) and a video going over some [troubleshooting](https://youtu.be/43VDcZQesHo) steps when using the FlashcatUSB xPort, I recommend watching both before doing anything. Those are both for using it in general, but it'll give you an idea of what to do.

# Hardware

## Soldering

The FlashcatUSB xPort Clip Adapters come partially assembled, the pin headers need to be soldered. Here's an example picture, ignore the flux residue.

![Soldering](/assets/img/FlashcatAdapters/Soldering.jpg){:class="img-responsive"}

## Tristate on NOR consoles

If your console is a NAND console you can skip this. If it's a NOR you'll need it.

For NOR consoles you have to solder a wire from the Tristate on the PS3 motherboard to a ground point. This could be a ground pin on the clip adapter, power supply, or to a ground point on the PS3 itself. Here are some pictures of the Tristate locations for different boards. Images from psdevwiki.com.

### DIA-001/DIA-002

![DIA-001_BOTTOM](/assets/img/DIA-001_BOTTOM.jpg){:class="img-responsive"}
![DIA-001_NOR](/assets/img/DIA-001_NOR.jpg){:class="img-responsive"}

### VER-001

![VER-001_BOTTOM](/assets/img/VER-001_BOTTOM.jpg){:class="img-responsive"}
![VER-001_NOR](/assets/img/VER-001_NOR.jpg){:class="img-responsive"}

### DYN-001

![DYN-001_BOTTOM](/assets/img/DYN-001_BOTTOM.jpg){:class="img-responsive"}
![DYN-001_NOR](/assets/img/DYN-001_NOR.jpg){:class="img-responsive"}

### SUR-001/JTP-001/JSD-001

![JTP-001_BOTTOM](/assets/img/JTP-001_BOTTOM.jpg){:class="img-responsive"}
![JSD-001_NOR](/assets/img/JSD-001_NOR.png){:class="img-responsive"}

I recommend soldering a wire to Tristate on the PS3 and taping it down, then only connect it to ground once you have everything else set up and your clip in place.
![TRISTATE](/assets/img/TRISTATE.jpg){:class="img-responsive"}

## Power

If you're using the power supply adapter use a 5v 2 Amp USB charger of some kind and a micro USB cable and plug it into it. You won't get enough power from plugging it into a USB port on your computer. Many Android phones use 5v 2 Amp USB chargers so they're easy to come by.
Your charger may say 2000ma instead, that's the same as 2 Amps. You can use chargers that are over 2 Amps, just 2 Amps is the recommended minimum.
![CHARGER](/assets/img/CHARGER.jpg){:class="img-responsive"}

If you're using some other external power supply disconnect the jumper on the clip adapter and connect the power supply to the appropriate positive and negative connections on it.

The flash memory in the PS3 uses 3.3v, you'll need to directly connect a power supply to the PS3 motherboard. Use the thickest gauge wire that makes sense and try to attach the wires as close as possible to the flash. Here's an example setup.

![PS3 SETUP](/assets/img/FlashcatAdapters/PS3_SETUP.jpg){:class="img-responsive"}

If you search for pictures of your motherboard you can usually find pictures of where the VCC and GND points are. If not you can use a multimeter to find them. Use the continuity mode and probe the exposed copper on the edge of the motherboard, then the probe test points near the flash to find a GND point. To find VCC probe a GND point then one of the capacitors connected to the flash, if there's no continuity then that's the VCC side. Probe that side of the capacitor then probe test points on the motherboard to find a VCC point to solder to.

# Software

Download my PS3 Downgrading Files FlashcatUSB Edition.zip, and extract it. Here's the [link](https://mega.nz/#!t3Z3SarA!HlAXxiMV5piTTSJMEBguUbMKgzVwIt6RpjK3qesoSys). Make sure to download the latest [FlashcatUSB Software](http://www.embeddedcomputers.net/software/) and replace the one I included.

Update the firmware on the FlashcatUSB xPort as well.

# [Continue to Page 5c - Downgrading With The FlashcatUSB xPort Clip Adapters]({{ "/PS3-Downgrading-With-The-FlashcatUSB-Clip-Adapters/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})
# [Troubleshooting the FlashcatUSB xPort Clip Adapters]({{ "/Troubleshooting-FlashcatUSB-xPort-Clip-Adapters/" | relative_url}})