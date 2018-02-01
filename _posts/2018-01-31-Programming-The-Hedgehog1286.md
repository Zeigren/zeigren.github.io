---
layout: post
title:  "Programming For The Hedgehog1286"
excerpt: "How To Program For The Hedgehog1286"
hedgehogguide: true
tag:
- Guide
- Hedgehog1286
- Programming
comments: false
---
# Programming For The Hedgehog1286
Since the Hedgehog1286 is pretty much a Teensy++ 2.0 clone (for the most part) any Teensy++ 2.0 firmware should be compatible with it. The only exception is if you're using all the program space, the Teensy++ 2.0 has a much smaller bootloader (~0.5k) then the Hedgehog1286 (~4k). But considering that there is 128k of space it's probably not an issue for most cases.

The Hedgehog1286 is also compatible with the Arduino IDE via Teensyduino, or you can of course write your code in Atmel Studio or some other way.

When using the Hedgehog1286 with 3.3v you'll only want to run the at90usb1286 at 8MHz, if using 5v then go ahead and run it at 16MHz.

--- 

# Arduino IDE
You'll of course need the [Arduino IDE](https://www.arduino.cc/en/Main/Software) and the [Teensyduino add-on](https://www.pjrc.com/teensy/teensyduino.html).

Now you can program for the Hedgehog1286 as if it were an Arduino (for the most part).

The pins have the same names as on the Teensy++ 2.0 which you can see [here](https://www.pjrc.com/teensy/pinout.html),you'll have to scroll down a bit. I'll make my own chart at some point.

The only thing that's different is you won't be able to flash the Hedgehog1286 directly from the Arduino IDE. You will have to compile your sketch as a .hex file and then flash it using one of the methods on the [Flashing The Hedgehog1286 page.]({{ "/Flashing-The-Hedgehog1286/" | relative_url}})

---

# Atmel Studio
You can of course program for the Hedgehog1286 using Atmel Studio. Just set it up for the at90usb1286 and you're good to go.

---

Have any questions or just want to talk about the Hedgehog1286? Head on over to the [Riot.im](https://riot.im) room at [#hedgehog1286:matrix.org](https://riot.im/app/#/room/#hedgehog1286:matrix.org). Or you can of course e-mail me or leave a comment on the forum thread of your choice.