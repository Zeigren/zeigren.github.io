---
layout: post
title:  "Update and the Hedgehog1286"
excerpt: "Unveiling of my at90USB1286 Development board, replacement for NORwegian Teensy"
news: true
tag:
- Hedgehog1286
- News
comments: true
---
![Hedgehog1286](/assets/img/HH1286/HHALL.jpg){:class="img-responsive"}

Here it is the Hedgehog1286 development board and expansions!

* [Hedgehog1286]({{ "/Hedgehog1286/" | relative_url}})    

* [Hedgehog1286 Info]({{ "/Hedgehog1286-Info/" | relative_url}})

* [Hedgehog1286 Expansions]({{ "/Hedgehog1286-Expansions/" | relative_url}})  

* [Hedgehog1286 Expansions Info]({{ "/Hedgehog1286-Expansions-Info/" | relative_url}})

---

This is my replacement for both the NORwegian Teensy Socket and Clip edition boards. It is the evolution of what would have been my Ultimate PS3 Downgrading Board.

After the release of the PS3 software downgrader I wasn't completely sure I would make an Ultimate Downgrade board, but there was still interest in the NORwegian Teensy boards for various reasons so I decided to go ahead and make something.

Obviously I took a different direction. Instead of making a board with a singular purpose I decided to make a development board that could instead use expansions giving it the same functionality as the NORwegian Teensy boards.

This way it can be used for other purposes when not reading/writing NANDs/NORs. Since it is based on the Atmel (Microchip) at90USB1286 it is pretty much a Teensy++ 2.0 clone and as such will be compatible with most Teensy++ 2.0 software/firmware.

However the Hedgehog1286 is not compatible with the Teensy Loader so to make flashing software/firmware to the Hedgehog1286 easier I made [DFUGUI](https://github.com/Zeigren/DFUGUI), which is just a front-end for [dfu-programmer](https://github.com/dfu-programmer/dfu-programmer). DFUGUI is also compatible with all the same microcontrollers that dfu-programmer supports so you can use it to flash software/firmware to other supported boards as well. DFUGUI is only for Windows but I believe there are already GUI's for dfu-programmer on Mac and Linux (I'll have to double check that). Otherwise you can just use dfu-programmer as is.

Currently the Hedgehog1286 boards are not for sale, I'm still in the process of testing them. From what testing I've done they should work just fine and I have no reason to believe that they won't. But I want to make sure of course. I've gone ahead and posted all of this as a way to update everyone that has been asking me about the NORwegian Teensy boards.

I've made a couple of [Riot.im](https://riot.im) rooms, one for discussing the Hedgehog1286 boards at [#hedgehog1286:matrix.org](https://riot.im/app/#/room/#hedgehog1286:matrix.org) as well as for DFUGUI at [+dfugui:matrix.org](https://riot.im/app/#/group/+dfugui:matrix.org). If you haven't used Riot.im it's kind of like an open source hybrid of Slack, Discord, and IRC. I definitely recommend checking it out.

03/03/2018