---
layout: post
title:  "Flashing The Hedgehog1286"
excerpt: "How To Flash Firmware Onto The Hedgehog1286"
hedgehogguide: true
tag:
- Guide
- Hedgehog1286
- Flashing
comments: false
---
# Flashing The Hedgehog1286

In order to flash a .hex file to the Hedgehog 1286 you have a couple of different options. You can use dfu-programmer directly, or DFUGUI on Windows. You can also use Atmel's FLIP program or just use Atmel Studio.

---

# DFUGUI

The [DFUGUI](https://github.com/Zeigren/DFUGUI) GitHub page.

* Grab the latest release, and launch DFUGUI.exe
* Hit the reset button on the Hedgehog1286
* Go to the AVR tab and pick at90usb1286
* Go to the erase tab and hit the erase button, this should open up the command line and erase the flash
* Exit the command line and click on the flash tab, and click on the flash button.
* This should open up a window to let you pick the .hex file you want to flash. Again this will open up the command line and flash the .hex file into memory.
* Exit the command line and click the launch button, that should execute the firmware you just uploaded to the Hedgehog1286. If not just unplug it and plug it back in.

---

# Atmel Studio

You should be able to just choose the at90usb1286 as your target and build and flash the code directly from Atmel Studio.

# [Troubleshooting]({{ "/Hedgehog1286-Troubleshooting/" | relative_url}})

---

Have any questions or just want to talk about the Hedgehog1286? Head on over to the [Riot.im](https://riot.im) room at [#hedgehog1286:matrix.org](https://riot.im/app/#/room/#hedgehog1286:matrix.org). Or you can of course e-mail me or leave a comment on the forum thread of your choice.