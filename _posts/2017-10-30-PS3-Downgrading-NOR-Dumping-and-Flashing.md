---
layout: post
title:  "PS3 Downgrading NOR Dumping and Flashing"
excerpt: "Dumping, Verifying, Patching, and Flashing NOR consoles"
guide: true
tag:
- Guide
- PS3 Downgrade
- NOR
- Dump
- Flash
- Patch
comments: false
---
## Using WAY-launchers To Dump NOR

**THIS IS IMPORTANT** Set the switch on the Clip Edition to NOR.

Now plug your Teensy++ 2.0 USB cable into your computer and the microUSB cable into the Clip Edition.

Open up the WAY-launcers folder and run WAY-launchers.exe.

Click on the NOR tab.

Then click on the Teensy++ 2.0 picture. Then pick the NORway.hex file, this will flash your Teensy++ 2.0 with the correct hex file. These should be in the same folder as WAY-launchers.

Then click Info. This should show information about your NOR. If it says unknown or has some other error go to the troubleshooting section.

Now you can click on the Dump tab. You want to change the Number of Dumps to 3, enable binary comparison, and save the dumps in the NOR DUMP ORIGINAL folder.

NOR dumps don't take that long, but it'll still be a few minutes to do all three.

If the binary comparison WAY-launchers does says that your dumps don't match up then something about your setup isn't working correctly, check the troubleshooting section.

## NOR Dumps
### Checking Your Dumps

Now you need to check those dumps. Leave your PS3 connected to everything and try not to disturb it, since we're just going to have to write back to it in a minute.

There are quite a few different dump checkers out there for PS3. There are two I primarily use.

BwE NOR Validator and PS3DumpChecker.

These two are usually enough for me. 

To be extra safe you can check with Norpatch that I included, and there are others out there you can use. You can also check manually using a hex editor. These are good things to consider doing.

Copy one of the dumps to the NOR DUMP COPIES folder.

### BwE Validator
Run BwE NOR Validator. Click start. You don't want to patch to 3.55 yet so press N, you also don't want to byte reverse so press N again.

Now it'll check your dump. After a little bit it will show you some quick results at the bottom. Ideally you want Warning: 0 and Danger: 0.

After you exit the program it'll open up a webpage with the full results of the check, it also saves those results as an html file. You should look over this to see where any of the Warning or Danger sections are. 

BwE hasn't been updated in awhile so if your errors are in the ROS0 and ROS1 sections that can be attributed to you having a newer firmware that it doesn't recognize.

### PS3DumpChecker
Run PS3DumpChecker. Check image, choose the dump you want to check. Don't patch the image.

If it says OK and the only errors you got with BwE were for ROS0 and ROS1 you are probably good to go. But if you end up with any errors check the troubleshooting section, google them, and then ask for help if you can’t figure it out.

You **absolutely need** good dumps before you can do anything else.

### Patching Your Dumps
Now that you’ve verified that your dumps are good, now we can patch them.

You have the option of either patching for 3.55 or to patch to immediately go to whatever CFW you’re going to use.

I normally downgrade all the way to 3.55 before doing anything else, you have to reformat your PS3 this way though, and boot into FSM (factory service mode).

But if you’re planning on just going to the latest CFW and don’t want to reformat your PS3 patching for CFW is a good choice, you don’t have to go into FSM, and it’s easier.

So make your choice.

To patch your dump for 3.55 run BwE NAND Validator again, but this time hit y to patch for 3.55. But hit n for the other stuff.

To patch your dump for CFW run PS3DumpChecker, check the image again but this time let it patch. It should patch it for noFSM 4.81 Ferrox.

Make sure in your NOR DUMP COPIES folder that you have a dump named something like dump_patched.bin.

### Writing Patched Dumps To The NOR
Now that you have your patched dump we need to write it back to your PS3. Hopefully you still have everything connected to your PS3 and it hasn't been disturbed.

Open WAY-launchers again. Then go to NOR Info and click start. Make sure it is still getting the correct Info for your NOR. If not something in your setup changed and you need to double check it, and check the troubleshooting section.

If it's fine go to the Write tab. Pick your patched dump file, click verify after write, then click start!

It'll take a minute or two to write and verify, if the verification checks out congratulations the hard part is over! If it doesn't go to the troubleshooting section.

# [Continue to Page 7 - PS3 Putting It Back Together]({{ "/PS3-Downgrading-PS3-Putting-It-Back-Together/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})