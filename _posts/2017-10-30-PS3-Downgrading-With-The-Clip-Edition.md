---
layout: post
title:  "PS3 Downgrading With The Clip Edition"
excerpt: "Using the Clip Edition to Downgrade"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- NORwegian Teensy Clip Edition
comments: false
redirect_to: https://docs.zeigren.com/books/ps3-downgrading/page/downgrading-with-the-clip-edition
---
# Downgrading With The Clip Edition

Don't have the Teensy++ 2.0 or power plugged in at first.
You'll probably want this open and a tab opened to either the NAND Dumping and Flashing page, or the NOR dumping and flashing page.

## Connecting The Clip

## NANDs

For NANDs you should dump NAND0 first. So connect the clip to that one first, then after you dump it do the same thing to NAND1.

### E3 Clip

The E3 clip was not designed for NANDs, but with a little know how you can anyway ;)

* Move the switch to NAND on the Clip Edition
* Plug the E3 clip into the NAND E3 connector. The outline around the connector should match the clip cable.
* The E3 clip can only go onto the NAND one way. The NAND has a little circle in one of the corners that you need to match up with the E3 clip like in the picture. I put a dot on my clip so I can just match it to the circle on the NAND. (Ignore the tape)
![E3BACK](/assets/img/E3BACK.jpg){:class="img-responsive"}
![E3CIRCLE](/assets/img/E3CIRCLE.jpg){:class="img-responsive"}

* This is where it gets a little tricky. You want to rest the inside lip of the E3 clip on the top of the NAND, keeping the clip at an angle. Then pull towards you while pressing down on the clip to seat it on the NAND.
![E3NANDANGLE](/assets/img/E3NANDANGLE.jpg){:class="img-responsive"}

* This is to ensure that the top pins on each side line up properly, since there are 8 more pins in the clip than there are on the NAND. So it's really easy to put the clip on with the wrong pins making contact.

* At this point you'll probably figure out that you need to trim the sides of the E3 clip so that way it can sit flush. It's hard to see but this is what mine looks like. You may also want to shave a little bit off that top inner lip if there is extra plastic on your NAND.
![E3PINS](/assets/img/E3PINS.jpg){:class="img-responsive"}
You just need it so the clip doesn't come into contact with the components around it.

* Now once you've whittled the clip down you'll want to be prepared. The clip does not like to stay where it's supposed to be *at all*. If you put the clip on and you hear a *click* then it's on wrong, the clip has slipped up and you're now on the second pin in the clip rather then the first.

* What "worked" for me was to have the Clip Edition hooked up to my computer with WAY-Launchers open (see the Dumping and Flashing pages) on the info screen so I could click start easily. I also had two pieces of tape, and some stuff I could put on the clip to hold it down.

* I would place the clip on and smoothly transition into pressing firmly down on the clip all while pushing towards the way you were just pulling. I would then click start on WAY-Launchers to see if I could get the Info of the chip. If I could that meant that I had a good connection.

* Repeat that until it works.

* Once it does work you don't want the clip to move *at all*. This is really hard to accomplish. I used two pieces of tape, one on the clip and one on the cable. That doesn't keep it in place, but keeps it close.
![E3NANDTAPE](/assets/img/E3NANDTAPE.jpg){:class="img-responsive"}

* Then I placed junk on top of the clip in order to put pressure on it. Then I moved that stuff around until I was able to get the Info using WAY-launchers again.
![E3NANDINSTALL](/assets/img/E3NANDINSTALL.jpg){:class="img-responsive"}
Yes that much stuff was *necessary* for it to work. You might be better off using a clamp.

Also putting the Clip Edition on something so it doesn't make contact with the PS3 motherboard is a good idea.

### 360 Clip 32 Pin

* Move the switch to NAND

* Plug the 32 pin 360 clip flat flex cable into the NAND 32 pin 360 clip connector.

* Put the clip on the NAND with the circles in the corners of both matched up
![360TOP](/assets/img/360TOP.jpg){:class="img-responsive"}

* Once the clip is on you need to make sure that it's firmly seated on the NAND, and apply pressure. Some people use clamps, others just sit something on top of it.

* If the clip makes contact with any of the components around the NAND you'll need to trim the sides of the clip. Don't do as bad of a job as I did, but you get the idea.
![360PINS](/assets/img/360PINS.jpg){:class="img-responsive"}

### 48 Pin UNI Clip

* Move the switch to NAND

* Plug the 48 Pin UNI Clip flat flex cable into the NAND 48 Pin UNI connector.

* Put the clip on the NAND with the circles in the corners of both matched up
![48UNITOP](/assets/img/48UNITOP.jpg){:class="img-responsive"}
![UNICIRCLE](/assets/img/UNICIRCLE.jpg){:class="img-responsive"}

* Once the clip is on you need to make sure that it's firmly seated on the NAND, and apply pressure.Some people use clamps, others just sit something on top of it.
![48UNIINSTALL](/assets/img/48UNIINSTALL.jpg){:class="img-responsive"}

* If the clip makes contact with any of the components around the NAND you'll need to trim the sides of the clip.
![48UNIPINS](/assets/img/48UNIPINS.jpg){:class="img-responsive"}

### 56 Pin UNI Clip

* Move the switch to NAND
* Plug the 56 Pin UNI Clip flat flex cable into the NAND 48 Pin UNI connector.
* Follow the E3 Clip Guide above

## NORs
### E3 Clip

* Move the switch to NOR

* Plug the E3 clip into the NOR E3 connector. The outline around the connector should match the clip cable.

* The E3 clip can only go onto the NOR one way. The NOR has a little circle in one of the corners that you need to match up with the E3 clip like in the picture. I put a dot on my clip so I can just match it to the circle on the NOR.(Ignore the tape)
![E3BACK](/assets/img/E3BACK.jpg){:class="img-responsive"}
![E3CIRCLE](/assets/img/E3CIRCLE.jpg){:class="img-responsive"}

* Once the clip is on you need to make sure that it's firmly seated on the NOR, and apply pressure. Some people use clamps, others just sit something on top of it.

* Depending on your clip you may need to trim the sides in order to clear the capacitors next to the NOR
![E3PINS](/assets/img/E3PINS.jpg){:class="img-responsive"}

### 56 Pin UNI Clip

* Move the switch to NOR
* Plug the 56 Pin UNI Clip flat flex cable into the NOR 56 Pin UNI connector.
* Make sure the circle on the clip matches up with the one on the NOR
* Once the clip is on you need to make sure that it's firmly seated on the NOR, and apply pressure. Some people use clamps, others just sit something on top of it.
* Depending on your clip you may need to trim the sides in order to clear the capacitors next to the NOR

If you have any problems check the troubleshooting section.

# [If You're Downgrading A NAND Continue - Page 6a]({{ "/PS3-Downgrading-NAND-Dumping-and-Flashing/" | relative_url}})
# [If You're Downgrading A NOR Continue - Page 6b]({{ "/PS3-Downgrading-NOR-Dumping-and-Flashing/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})