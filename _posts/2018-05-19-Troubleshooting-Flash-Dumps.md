---
layout: post
title:  "Troubleshooting Flash Dumps"
excerpt: "Some troubleshooting tips for flash dumps"
fcadaptersguide: true
tag:
- Guide
- FlashcatUSB
- xPort
- Resources
comments: false
redirect_to: https://docs.zeigren.com/books/flashcatusb-clip-adapters/page/troubleshooting
---
# Some Tips

* Double check that the flash dump has any data in it. You can do this in the Flashcat software itself or a third party hex editor like HxD. Make sure that the data isn't all 0's, F's, or something like that (unless that is what you're expecting to get, like a blank flash). If it is there's likely a power issue with your setup, although it could be a clip issue as well
* In HxD you can use Analysis > Statistics as another way to see what the dump consists of
* I recommend dumping the flash three times and comparing those, you can use the FlashcatUSB software to do comparisons. You can also use something like md5Checker to see if the md5 checksums of the dumps match up
* If none of the dumps match up there's something wrong with your setup, if two of the three match-up those are most likely correct but I would double check by dumping the flash again

---

Have any questions or just want to talk about the FlashcatUSB xPort Clip Adapters? Head on over to the [Riot.im](https://riot.im) room at [#FCXAdapters:matrix.org](https://riot.im/app/#/room/#FCXAdapters:matrix.org). You can also visit the [BlackCatUSB](https://www.blackcatusb.net/index.php) forum where there's already a [thread](https://www.blackcatusb.net/index.php?threads/tsop56-48-nor-nand-clip-adapters-for-the-flashcatusb-xport.493/) for the adapters. Or you can of course e-mail me or leave a comment on the forum thread of your choice.
