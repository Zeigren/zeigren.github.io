---
layout: post
title:  "PS3 Downgrading NOR Dumping and Flashing"
excerpt: "Dumping, Verifying, Patching, and Flashing NOR consoles"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- NOR
- Dump
- Flash
- Patch
comments: false
redirect_to: https://docs.zeigren.com/books/ps3-downgrading/page/nor-dumping-and-flashing
---
## Using WAY-launchers To Dump NOR

**THIS IS IMPORTANT** Set the switch on the Clip Edition to NOR.

If you didn't download it earlier here's the zip file with the exact folder structure I use, and with all the files you need inside of it.

You can [download it here](https://mega.nz/#!ovIEhS5D!Eke5679s1qnOJEv8Bs3BSBIGjsHzn5Zzmj0-w6hrAk4)

Unzip the PS3 Downgrading Files you downloaded, and install the files in the install first folder.
![InstallFirst](/assets/img/InstallFirst.PNG){:class="img-responsive"}

Now plug your Teensy++ 2.0 USB cable into your computer and the microUSB cable into the Clip Edition.

Open up the WAY-launchers folder and run WAY-launchers.exe.
![waylauncherfolder](/assets/img/waylauncherfolder.PNG){:class="img-responsive"}

Click on the NOR tab.
![waylaunchersnor](/assets/img/waylaunchersnor.PNG){:class="img-responsive"}

Then click on the Teensy++ 2.0 picture. Then pick the NORway.hex file, this will flash your Teensy++ 2.0 with the correct hex file. These should be in the same folder as WAY-launchers.
![norwayhex](/assets/img/norwayhex.PNG){:class="img-responsive"}
![norwayhexprogram](/assets/img/norwayhexprogram.PNG){:class="img-responsive"}

Then click Info. This should show information about your NOR. If it says unknown or has some other error go to the troubleshooting section.

Now you can click on the Dump tab. You want to change the Number of Dumps to 3, enable binary comparison, and save the dumps in the NOR DUMP ORIGINAL folder.
![NORDUMP](/assets/img/NORDUMP.PNG){:class="img-responsive"}

NOR dumps don't take that long, but it'll still be a few minutes to do all three.

If the binary comparison WAY-launchers does says that your dumps don't match up then something about your setup isn't working correctly, check the troubleshooting section.

## Using the FlashcatUSB Software To Dump NORs

You'll open up the FlashcatUSB Software, make sure that you have the settings correct.

Under Mode > Protocol Settings
![Protocol Settings](/assets/img/FlashcatAdapters/Protocol Settings.png){:class="img-responsive"}

Detect the NOR and read the NOR to a bin file and save it into the NOR DUMPS ORIGINAL folder.

I would read the NOR at least two times then use md5checker to check that they match, or you can use the built in comparison tool in the FlashcatUSB software to do the same thing.

## NOR Dumps
### Checking Your Dumps

Now you need to check those dumps. Leave your PS3 connected to everything and try not to disturb it, since we're just going to have to write back to it in a minute.

Copy a NOR.bin from the NOR DUMP ORIGINAL folder, and paste those into NOR DUMP COPIES.
![NORDUMPCOPIES](/assets/img/NORDUMPCOPIES.PNG){:class="img-responsive"}

There are quite a few different dump checkers out there for PS3. There are two I primarily use.

BwE NOR Validator and PS3DumpChecker.

These two are usually enough for me.

I included Norpatch that you can also check with, and there are others out there you can use. You can also check manually using a hex editor. These are good things to consider doing.

### BwE Validator

Run BwE NOR Validator. Click start. You don't want to patch to 3.55 yet so press N, you also don't want to byte reverse so press N again.
![BwENOR](/assets/img/BwENOR.PNG){:class="img-responsive"}
![BwENORNO](/assets/img/BwENORNO.PNG){:class="img-responsive"}

Now it'll check your dump. After a little bit it will show you some quick results at the bottom. Ideally you want Warning: 0 and Danger: 0.
![BwEQuickResults](/assets/img/BwEQuickResults.PNG){:class="img-responsive"}

After you exit the program it'll open up a webpage with the full results of the check, it also saves those results as an html file. You should look over this to see where any of the Warning or Danger sections are.

BwE hasn't been updated in awhile so if your errors are in the ROS0 and ROS1 sections that can be attributed to you having a newer firmware that it doesn't recognize.
![BwEROS0](/assets/img/BwEROS0.PNG){:class="img-responsive"}
![BwEROS1](/assets/img/BwEROS1.PNG){:class="img-responsive"}
![BwEMD5](/assets/img/BwEMD5.PNG){:class="img-responsive"}
![BwEOther](/assets/img/BwEOther.PNG){:class="img-responsive"}

### PS3DumpChecker

Run PS3DumpChecker. Check image, choose the dump you want to check. Don't patch the image.
![PS3DumpChecker](/assets/img/PS3DumpChecker.PNG){:class="img-responsive"}

If it says OK and the only errors you got with BwE were for ROS0 and ROS1 you are probably good to go. But if you end up with any errors check the troubleshooting section, google them, and then ask for help if you can’t figure it out.

You **absolutely need** good dumps before you can do anything else.

### Patching Your Dumps

Now that you’ve verified that your dumps are good, now we can patch them.

If using a Teensy you have the option of either patching for 3.55 or to patch to go to CFW. If using the FlashcatUSB xPort you'll need to go straight to CFW.

I normally downgrade all the way to 3.55 before doing anything else, you have to reformat your PS3 this way though, and boot into FSM (factory service mode).

But if you’re planning on just going to the latest custom firmware and don’t want to reformat your PS3 patching for CFW is the way to go, you don’t have to go into FSM either, and it’s easier.

So make your choice.

To patch your dump for 3.55 run BwE NAND Validator again, but this time hit y to patch for 3.55. But hit n for the other stuff.

To patch your dump for CFW run PS3DumpChecker, check the image again but this time let it patch. It should patch it for noFSM Ferrox.

Make sure in your NOR DUMP COPIES folder that you have a dump named something like NOR_patched.bin.

### Writing Patched Dumps To The NOR With WAY-Launchers

Now that you have your patched dump we need to write it back to your PS3. Hopefully you still have everything connected to your PS3 and it hasn't been disturbed.

Open WAY-launchers again. Then go to NOR Info and click start. Make sure it is still getting the correct Info for your NOR. If not something in your setup changed and you need to double check it.

If it's fine go to the Write tab. Pick your patched dump file, click verify after write, then click start!
![NORwrite](/assets/img/NORwrite.PNG){:class="img-responsive"}

### Writing Patched Dumps To NOR Using FlashcatUSB

Open up the FlashcatUSB software and write the new.bin to the NOR. To speed it up you can turn off verify programming under the Mode tab. Although I recommend verifying the write after it's finished.

# [Continue to Page 7 - PS3 Putting It Back Together]({{ "/PS3-Downgrading-PS3-Putting-It-Back-Together/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})