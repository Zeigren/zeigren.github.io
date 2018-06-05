---
layout: post
title:  "Troubleshooting the FlashcatUSB Clip Adapters"
excerpt: "Some troubleshooting tips"
fcadaptersguide: true
tag:
- Guide
- FlashcatUSB
- xPort
- Resources
comments: false
---
# First Steps

The majority of the problems with using the clips are from the clips making poor contact and from power issues. If other components besides the flash are receiving power they may try to access the flash at the same time, which would also cause issues. If that is the case then you'll have to figure out how to prevent the other chip from doing that, usually by putting it into a reset state or tri-state.

Unfortunately with so many variables it can be difficult to pin down exactly what the problem is. I would start with trying to fix any power problems since they are more straight forward, then moving on to the clips.

If the flash is being detected but isn't found in the library that means that the FlashcatUSB is receiving some data from the flash but for some reason isn't receiving the correct Chip ID.

* Make sure the FlashcatUSB is set to the appropriate voltage for the flash you're trying to read/write, and if you're using the power supply adapter make sure that it is as well
* Make sure it is set to Parallel Flash Mode, and if you are reading a NAND make sure in protocol settings that the NAND settings are correct for your setup
* Open the console tab and look for something like this: Connected to Flash (CHIP ID: 0x00000000)
* You can use the Chip ID for some clues as to what is going on. Every time you change something you'll want to try and detect the flash again (press F1), and see how this number changes
* If the flash is detected it will say so in the console
* Double check that the flash you are trying to read/write is on the [supported list](http://www.embeddedcomputers.net/products/FlashcatUSB_xPort/)

# Power Problems

The wires that are in the clip cables are really thin and are often unable to supply adequate power to the flash while it is still soldered to a device.

## Things you can try

* Check the power supply output voltage with a multi-meter to make sure it's correct
* Directly connect your power supply to the device you are trying to read/write the flash from, try to do this as close to the flash as possible and with the largest gauge wire that is reasonable for your situation. Check nearby test points and see if they're connected to VCC(+) or GND(-) and solder wires to those, otherwise you may need to solder wires onto a nearby capacitor or some other component

### If you have the power supply adapter

* Check if the input voltage from the USB charger is 5v. The input voltage should work down to 4.5v, but the closer it is to 5v the better
* Try a different USB charger, I recommend a 2 amp charger or higher. You might have problems with chargers that are under 2 amps. Or just have a charger that isn't so great
* Try a different microUSB cable
* Reseat the voltage selection jumper

### If you're using an external power supply

* It might be too noisy or might sag under load, you can put the optional capacitor on the clip adapters to try and mitigate this

# Poor Clip Contact

## Things you can try

* Make sure the clip is on the right way, dot on the clip matched up to the dot on NOR/NAND
* Clean the legs on the NOR/NAND with isopropyl alcohol
* Trim the sides of the clip if they're hitting any components next to the NOR/NAND
* Reseat the clip and any cables
* Make sure you're applying even pressure to the clip, sometimes it takes a lot of pressure
* Make sure that your setup is stable, you don't want things moving around while you're trying to read/write the flash
* Move the clip around while it's on the NOR/NAND

### Examples of Trimmed Clips

![E3PINS](/assets/img/E3PINS.jpg){:class="img-responsive"}
![360PINS](/assets/img/360PINS.jpg){:class="img-responsive"}
![48UNIPINS](/assets/img/48UNIPINS.jpg){:class="img-responsive"}

If you need to trim the clips because of components around the flash be careful, it's easy to mess up the pins doing this.

### Matching Dots

![E3CIRCLE](/assets/img/E3CIRCLE.jpg){:class="img-responsive"}
![UNICIRCLE](/assets/img/UNICIRCLE.jpg){:class="img-responsive"}

### Applying Pressure

![48UNIINSTALL](/assets/img/48UNIINSTALL.jpg){:class="img-responsive"}

It can take a lot of force to get a good connection. My clips are pretty beat up from all of my testing so hopefully you won't need to use as much force.

# Last Resort

* Use a needle or some other small pointy thing to push the pins on the clip further out, obviously be careful it's easy to mess up the pins

# E3 NAND Clip Extra Considerations

The E3 clip was not designed for NANDs, but with a little know how you can anyway ;)

* The E3 clip can only go onto the NAND one way. The NAND has a little circle in one of the corners that you need to match up with the E3 clip like in the picture. I put a dot on my clip so I can just match it to the circle on the NAND. (Ignore the tape)

![E3BACK](/assets/img/E3BACK.jpg){:class="img-responsive"}
![E3CIRCLE](/assets/img/E3CIRCLE.jpg){:class="img-responsive"}

* This is where it gets a little tricky. You want to rest the inside lip of the E3 clip on the top of the NAND, keeping the clip at an angle. Then pull towards you while pressing down on the clip to seat it on the NAND.

![E3NANDANGLE](/assets/img/E3NANDANGLE.jpg){:class="img-responsive"}

* This is to ensure that the top pins on each side line up properly, since there are 8 more pins in the clip than there are on the NAND. So it's really easy to put the clip on with the wrong pins making contact.
* The clip does not like to stay where it's supposed to be *at all*. If you put the clip on and you hear a *click* then it's on wrong, the clip has slipped up and you're now on the second pin in the clip rather then the first.
* I would place the clip on and smoothly transition into pressing firmly down on the clip all while pushing towards the way you were just pulling. I would then try and detect the flash. If I could that meant that I had a good connection.
* Repeat that until it works.
* Once it does work you don't want the clip to move *at all*. This is really hard to accomplish. I used two pieces of tape, one on the clip and one on the cable. That doesn't keep it in place, but keeps it close.

![E3NANDTAPE](/assets/img/E3NANDTAPE.jpg){:class="img-responsive"}

* Then I placed junk on top of the clip in order to put pressure on it. Then I moved that stuff around until I was able to get it to detect again.

![E3NANDINSTALL](/assets/img/E3NANDINSTALL.jpg){:class="img-responsive"}
Yes that much stuff was *necessary* for it to work. You might not need that much pressure or be better off using a clamp.

---

Have any questions or just want to talk about the FlashcatUSB xPort Clip Adapters? Head on over to the [Riot.im](https://riot.im) room at [#FCXAdapters:matrix.org](https://riot.im/app/#/room/#FCXAdapters:matrix.org). You can also visit the [BlackCatUSB](https://www.blackcatusb.net/index.php) forum where there's already a [thread](https://www.blackcatusb.net/index.php?threads/tsop56-48-nor-nand-clip-adapters-for-the-flashcatusb-xport.493/) for the adapters. Or you can of course e-mail me or leave a comment on the forum thread of your choice.
