---
layout: post
title:  "PS3 Downgrading NAND Dumping and Flashing"
excerpt: "Dumping, Verifying, Patching, and Flashing NAND consoles"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- NAND
- Dump
- Flash
- Patch
comments: false
---

## Using WAY-launchers To Dump NANDs

**THIS IS IMPORTANT** Set the switch on the Clip Edition to NAND.

If you didn't download it earlier here's the zip file with the exact folder structure I use, and with all the files you need inside of it.

You can [download it here](https://mega.nz/#!ovIEhS5D!Eke5679s1qnOJEv8Bs3BSBIGjsHzn5Zzmj0-w6hrAk4)

Unzip the PS3 Downgrading Files you downloaded, and install the files in the install first folder.
![InstallFirst](/assets/img/InstallFirst.PNG){:class="img-responsive"}

Now plug your Teensy++ 2.0 USB cable into your computer and the microUSB cable into the Clip Edition.

Open up the WAY-launchers folder and run WAY-launchers.exe.
![waylauncherfolder](/assets/img/waylauncherfolder.PNG){:class="img-responsive"}

Click on the NAND tab.
![NANDWAY](/assets/img/NANDWAY.PNG){:class="img-responsive"}

Then click on the Teensy++ 2.0 picture. Then pick the appropriate NANDway_SignalBoosterEdition.hex file, this will flash your Teensy++ 2.0 with the correct hex file using Teensy_Cli.exe. These should be in the WAY-launchers folder.
![NANDWAYSBEhex](/assets/img/NANDWAYSBEhex.PNG){:class="img-responsive"}
![NANDwaySBEhexProgram](/assets/img/NANDwaySBEhexProgram.PNG){:class="img-responsive"}

Then click Info. This should show information about your NAND. If it says unknown or has some other error go to the troubleshooting section.
![NANDINFO](/assets/img/NANDINFO.PNG){:class="img-responsive"}

Now you can click on the Dump tab. You want to change the Number of Dumps to 3, enable binary comparison, and save the dumps in the NAND DUMPS ORIGINAL folder. If you're dumping NAND0 I would name it either NAND0 or NANDTOP and if it's NAND1 I would name it NAND1 or NANDBOTTOM, that way you don't confuse them later.
![NANDDUMP](/assets/img/NANDDUMP.PNG){:class="img-responsive"}
![NANDDUMPING](/assets/img/NANDDUMPING.PNG){:class="img-responsive"}

NAND dumps can take like 20 minutes each. So feel free to go do something else for awhile.

If the binary comparison WAY-launchers does after all three dumps are complete says that your dumps don't match up then something about your setup isn't working correctly. Try using the md5 checker on the three dumps to see if they all have different md5 sums. If two of them match up then those might be correct, and the third one might just be an outlier. If that's the case do one more dump and then check if the md5 sum of that dump matches the other two, if it does then you're probably good.

If not check the troubleshooting section.

Now that you've dumped one NAND dump the other.

## NAND Dumps
### Join Your Dumps Together
Leave your PS3 connected to everything and try not to disturb it, since we're just going to have to write back to it in a minute.

Once you have dumps of both NAND0 and NAND1 you have to join them together into a single dump.

Copy a NAND0.bin, and a NAND1.bin from the NAND DUMP ORIGINAL folder, and paste those into NAND DUMP COPIES.
![NANDDUMPCOPIES](/assets/img/NANDDUMPCOPIES.PNG){:class="img-responsive"}

In NAND DUMP COPIES open FlowRebuilder.exe 

* Choose UNSCRAMBLE then interleave two NAND flashes into one unified dump.
* Select your NAND0 dump for Flash0(TOP) and NAND1 dump for Flash1(Bottom).
(Remember NAND0 is the NAND that is on the same side of the motherboard as the CPU.
NAND1 is the NAND that is on the same side of the motherboard the Blu-Ray Drive connects to.)
* Then select to save the output in the NAND DUMP COPIES folder. I recommend saving it as something like NANDmerged.
* Then execute operation
* FlowRebuilder will tell you if you have any bad blocks, it'll also throw up an error if something went wrong
* If you get an error that says it can't complete the merge, try merging them again in FlowRebuilder except switched. Input NAND1 instead of NAND0, and NAND0 instead of NAND 1. You might have just got the two mixed up. If that's the case then remember that! I would recommend renaming them right away to what they're supposed to be if that works, otherwise you're going to have a lot of heartache later on.
* Also it's normal to have a few bad blocks, you just don't want a ton of them
![Flowrebuilder](/assets/img/Flowrebuilder.PNG){:class="img-responsive"}

### Verify NAND
Now you need to check your merged NAND.

There are quite a few different dump checkers out there for PS3. There are two I primarily use.

BwE NAND Validator and PS3DumpChecker.

These two are usually enough for me. 

I added norpatch that you can also check with. You can also check manually using a hex editor. These are good things to consider doing.

### BwE Validator
Run BwE NAND Validator. Pick the merged dump, and just hit N for all the options it gives you.
![BwENAND](/assets/img/BwENAND.PNG){:class="img-responsive"}

Now it'll check your dump. After a little bit it will show you some quick results at the bottom. Ideally you want Warning: 0 and Danger: 0.
![BwEQuickResults](/assets/img/BwEQuickResults.PNG){:class="img-responsive"}

After you exit the program it'll open up a webpage with the full results of the check, it also saves this as an html file you can look at later. You should look over this to see where any of the Warning or Danger sections are. 

BwE hasn't been updated in awhile so if your errors are in the ROS0 and ROS1 sections that can be attributed to you having a newer firmware that it doesn't recognize.
![BwEROS0](/assets/img/BwEROS0.PNG){:class="img-responsive"}
![BwEROS1](/assets/img/BwEROS1.PNG){:class="img-responsive"}
![BwEMD5](/assets/img/BwEMD5.PNG){:class="img-responsive"}
![BwEOther](/assets/img/BwEOther.PNG){:class="img-responsive"}

### PS3DumpChecker
Run PS3DumpChecker. Check image, choose the merged dump you want to check. Don't patch the image.
![PS3DumpChecker](/assets/img/PS3DumpChecker.PNG){:class="img-responsive"}

If it says OK and the only errors you got with BwE were for ROS0 and ROS1 you are probably good to go. But if you end up with any errors check the troubleshooting section, google them, and then ask for help if you can't figure it out. 

You **absolutely need** good dumps before you can do anything else.

### Patching Your Dumps
Now that you've verified that your dumps are good, now you can patch them.

You have the option of either patching for 3.55 or to patch to go to CFW.

I normally downgrade all the way to 3.55 before doing anything else, you have to reformat your PS3 this way though, and boot into FSM (factory service mode). 

But if you're planning on just going to the latest custom firmware and don't want to reformat your PS3 patching for CFW is the way to go, you don't have to go into FSM either, and it's easier. 

So make your choice.

To patch your merged dump for 3.55 run BwE NAND Validator again, but this time hit y to patch for 3.55. But hit n for the other stuff.

To patch your merged dump for CFW run PS3DumpChecker, check the image again but this time let it patch. It should patch it for noFSM 4.81 Ferrox.

Make sure that in your NAND DUMP COPIES folder you have a dump named something like merged_patched.bin.

### Split Merged Dump
Now that you checked your dump and it's good to go you have to split it back up again before you flash it to your PS3.

So open FlowRebuilder again.

Choose RE-SCRAMBLE a modified dump then de-interleave it into two new flashes.

For Flash0 (TOP) and Flash1 (Bottom), choose the same dumps you chose for those the first time. 

Then for the interleaved modified file choose your merged_patched.bin.

Now execute operation.

In the folder your dumps are in you should now have something like NAND0.bin.new.bin and NAND1.bin.new.bin. Those are the files you're going to be reflashing to your PS3.

### Writing Patched Dumps To NANDS
Hopefully your still connected to your PS3 and it hasn't been disturbed in anyway.

Open WAY-launchers.exe again.

Go to the NAND tab, and Info then click Start. Make sure you still have a good connection to your PS3. If you don't reseat everything.

Now go to the Write Tab.

For the dump file you're going to pick the new.bin of the NAND you're currently connected to.

Then you will also click Use Diff. file, the Diff. file will be in NAND DUMP COPIES folder, in a folder called Differential Flashing. Pick Flash0(TOP) or Flash1(BOTTOM) depending on which NAND you're currently connected to.

Then Click verify after write, and then Start!

![NANDwrite](/assets/img/NANDwrite.PNG){:class="img-responsive"}

Using a diff. file it only takes like 2 minutes to write a NAND. So once that's done and it verifies correctly you now have to do the same thing to the NAND on the other side of the motherboard.

Now the hard part is done!

If you had any problems check the troubleshooting section.

# [Continue to Page 7 - PS3 Putting It Back Together]({{ "/PS3-Downgrading-PS3-Putting-It-Back-Together/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})