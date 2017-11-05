---
layout: post
title:  "PS3 Downgrading Final Steps"
excerpt: "You're Almost Done!"
guide: true
tag:
- PS3 Downgrade
- Guide
- Final
comments: false
---
# Finishing The Downgrade
You are so close to being done!

So there are two routes you can take from here.

If you chose to patch to 3.55 using BwE then follow the Downgrade to 3.55 section.

If you chose to noFSM patch using PS3DumpChecker then follow Downgrade to CFW section.

## Downgrade to 3.55
You'll need go into FSM in order to flash down to 3.55. Luckily you can just use the Teensy++ 2.0 to do this! 

Go into the FSM folder and run the Teensy Loader (Teensy.exe), open hex file and choose psgrade_at90usb1286_8Mhz_teensy++_2.0_noLED.hex. Hit the reset button on the Teensy++ 2.0. Then hit program. Once it's done hit reboot.

Unplug your Teensy++ 2.0 from your computer, and while your PS3 is off plug the Teensy++ 2.0 into the right most USB port on your PS3.

Now you'll need to turn your PS3 on and immediately hit the eject button, but don't press both at the same time. If it boots to XMB then you didn't do it fast enough.

Your PS3 should turn on for a little bit then turn off on its own.

Now you unplug the Teensy++ 2.0 from the PS3.

You need to put some files onto a flash drive that has been formatted to FAT32 that you'll then insert into your PS3. The files will be in the 'Get Into FSM folder'.

Put those onto a USB flash drive, and put the flash drive in the right most USB port of your PS3.

Turn on your PS3, it should have a black screen but your HDD activity light should be blinking. After a while your PS3 will turn off.

Remove the USB drive and put it back into your computer. There should be a file called UPDATER_LOG on it. Check it and at the bottom it should say 0x83manufacturing updating SUCCESS(0x8002f000).

You now need to get your PS3 out of FSM. Delete the files on your USB drive. Go to the 'Get Out Of FSM files' and put them on your USB drive. Put the USB drive into the right most port in your PS3. Turn your PS3 on, it should turn on for a little bit then turn off again. Remove the USB drive. Now you should be on rogero 3.55 spoofed to 4.11.

### QA Flag De-Hashing
This is the final step in getting down to 3.55 OFW. It's also done in order to prevent bricking.

Delete the files on your USB drive. Put the files in the 'QA Flag De-Hashing' folder onto it. Put the USB drive into your PS3.

Turn on your PS3. Install QA toggle from XMB under homebrew - THEN run it from GAME, your PS3 should beep three times.

If you get a blank screen you have a problem with your blu-ray drive, see the troubleshooting section.

Now check if your PS3 is QA flagged. Go to the Network Settings and while it's selected press L1 + L2 + L3 + R1 + R2 + dpad down all at the same time.

If you are QA flagged a new option will show up under network settings.

Turn off your PS3.

Boot into recovery mode.
* To boot into recovery mode turn your PS3 off. Now hold the power button until you get a beep, then a second beep and your PS3 will turn off. 
* Press and hold the power button again until you get one beep, then a second beep and then let go of the power button. It should boot into recovery.
* Select "6. System Update" to reinstall the firmware.

If it works fine your PS3 will reboot, and be succesfully dehashed and downgraded to OFW 3.55!

Now if you want to install a CFW you can.

Check the Choosing a CFW section below if you don't know what CFW you want.

Copy the CFW you want to use to a USB drive and put it in a UPDATE folder inside a PS3 folder.

Plug that into the right most USB port. Make sure there isn't a disc in the Blu-Ray drive. Then install the update from XMB under Update, Install from Mass Storage Device.

You'll now be on whatever CFW you chose.

## Downgrade to CFW
Turn on your PS3.

If your PS3 is booting to a black screen you need to enter recovery.
* To boot into recovery mode turn your PS3 off. Now hold the power button until you get a beep, then a second beep and your PS3 will turn off. 
* Press and hold the power button again until you get one beep, then a second beep and then let go of the power button. It should boot into recovery.
* Select "6. System Update" to reinstall the firmware.

Once your PS3 boots fine, copy the CFW you want to use to a USB drive and put it in a UPDATE folder inside a PS3 folder.

Check the Choosing a CFW section below if you don't know what CFW you want.

Plug that into the right most USB port. Make sure there isn't a disc in the Blu-Ray drive. Then install the update from XMB under Update, Install from Mass Storage Device.

You'll now be on whatever CFW you chose.

## Choosing A CFW

So there's a lot of options for CFW out there. Luckily there are also a lot of good guides out there for them too.

I'll cover some basics.

A quick rundown of what all these different terms mean.

* CFW is Custom Firmware
* OFW is Official/Retail Firmware
* CEX is consumer or retail consoles
* DEX is Debug/developer consoles
* REX is the Rebug Custom Firmware for CEX(Consumer)
* D-REX is the Rebug Custom Firmware for DEX(Developer)

If you don't need all the developer options, or don't know if you need all the developer options I recommened going with the REX Rebug firmware. This is what the majority of people with modded PS3's use.

Here's a link to the [Rebug](https://rebug.me/) website where you can download the latest Rebug firmware.

# CONGRATULATIONS YOU'RE DONE

# [More Info]({{ "/PS3-Downgrading-More-Info/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})