---
layout: post
title:  "PS3 Downgrading Troubleshooting"
excerpt: "Troubleshooting All The Problems"
ps3guide: true
tag:
- Guide
- PS3 Downgrade
- Troubleshooting
comments: false
---
# Troubleshooting the NORwegian Teensy Clip Edition
## Poor Clip Contact

* Unknown Chip Errors
* Dumps not matching up in WAY-launchers
* Getting lots of errors when you verify them in BwE or PS3DumpChecker
* Errors when you try to verify after writing the NOR/NAND
* Incredibly slow read/write speeds


Most of the problems from using clips is from the clips not making a good connection with the NOR or NAND.

Especially when using the clips made for NORs with NANDs, you need to make sure that the the top pins on the clips are making contact with the top pins on the NAND.

Poor clip connections will cause most of the problems with reading/writing to the NOR/NAND, as well as the majority of errors that you get when you check your dumps. So try these steps first and then repeatedly reseating the clips before moving on to the other sections.

### Things you can try
* Make sure the clip is the right way, dot on clip matched up to dot on NOR/NAND
* Clean the legs on the NOR/NAND with isopropyl alcohol
* Use a needle or some other small pointy thing to push the pins on the clip further out, obviously be careful it's easy to mess up the pins
* Trim the sides of the clips if they're hitting any components next to the NOR/NAND
* Reseat the cables
* Make sure you're applying even pressure to the clip
* Make sure that you're setup is stable, you don't want things moving around while you're trying to flash/dump

## Power Problems

* Unknown Chip Errors
* Dumps not matching up in WAY-launchers
* Getting lots of errors when you verify them in BwE or PS3DumpChecker
* Errors when you try to verify after writing the NOR/NAND
* Incredibly slow read/write speeds
* Teensy Not Being Recognized
* High Pitch Whine

After the clips having poor connections the next thing is power problems. With the Clip Edition I've mitigated this quite a bit. The clip edition is capable of providing enough stable power that their shouldn't be an issue. But that doesn't mean there still can't be a problem.

Power problems can cause most of the same issues as bad clip connections, just the bad clip connections are more likely.

If your Clip Edition has a high pitch whine, unplug both USB cables. There is a short between 3.3v and GND on the board. You can confirm this by checking for continuity using a multimeter between GND and 3.3v. Make sure the NAND/NOR switch isn't stuck somewhere between the two. Check if there are any debris stuck in between pins on the board, or around any capacitors.

### Things you can try
* If you're using an external power supply it might be too noisy, I recommend powering the NORwegian Teensy Clip Edition over microUSB.
* Check for 3.3v at the external power headers while the microUSB cable is plugged in. If you're not getting 3.2v to 3.4v there might be a problem with the onboard regulator, or the USB charger you're using.
* Check if you're getting 5v from the USB charger. Use a multimeter and check between 'GND' and this side of the capacitor 'CIN'. You can use the outside of the USB port as 'GND', or any other 'GND' point on the board.
![POWER](/assets/img/POWER.jpg){:class="img-responsive"}
* Try a different USB charger, I recommend a 2 amp charger or higher. You might have problems with chargers that are under 2 amps. Or just have one that isn't so great.
* Also try a different microUSB cable.
* If you're using a Teensy++ 2.0 that already has a voltage regulator on it make sure that the 5v hole/pin on the Teensy++ 2.0 is disconnected from the NORwegian Teensy Clip Edition

## Software Problems
* WAY-launchers/NORway/NANDway can't find or connect to Teensy++ 2.0
* Anti-Virus Software says WAY-launchers is a virus

If you downloaded my PS3 Downgrading Files then everything you need should be in the right place. So the main problems will be with installing python 2.7.2, pyserial 2.5, and serial_install (the Teensy++ 2.0 serial drivers). Try reinstalling those with admin privileges.

Try using a different mini-USB cable to the Teensy++ 2.0. Also try a different USB port. Make sure it's directly connected to your computer and not going through a USB hub.

Some AV software may say that WAY-launchers is a virus, this is just a false positive. With how WAY-launchers is designed it actually has other .exe files that it unpacks and uses for downgrading, this is why the AV software thinks it's a virus.

But all these .exe files are open source, and you can go on github and check them out for yourself if you don't think they're safe. One is the Teensy_Cli.exe, which it uses to flash the .hex files to the Teensy++ 2.0, this is made by PJRC the creators of the Teensy++ 2.0. The other one is called COMMANDS.EXE which it uses to control NORway.py and NANDway_SignalBoosterEdition.py, which actually do all the work of reading/writing to the NOR/NAND of the PS3. COMMANDS.EXE is actually just a batch script that was converted to an .exe, you can view the batch script on the WAY-launchers github page.

## Other Connectivity Problems
* Unknown Chip Errors
* Dumps not matching up in WAY-launchers
* Getting lots of errors when you verify them in BwE or PS3DumpChecker
* Errors when you try to verify after writing the NOR/NAND
* Incredibly slow read/write speeds

If you're still having problems this is the next step.

* If you're downgrading a NOR make sure that you're getting a good connection between Tristate and the Teensy++ 2.0. Use a multimeter and check between the Tristate connection on your PS3, and pin E7 on the Teensy++ 2.0. If there isn't continuity resolder your Tristate connection.
* Check that your Teensy++ 2.0 is making a good connection with the NORwegian Teensy Clip Edition. This will be tedious but you can use a multimeter and probe each connection on the Teensy++ 2.0 itself and then the corresponding pin on the NOR UNI Clip connector. This applies to whatever clip your using, I just chose that connector because it's easier.

Here's the pinout


NOR | Teensy++ 2.0
---|---
1	|Not Used
2	|B6
3	|PA7
4	|PA6
5	|PA5
6	|PA4
7	|PA3
8	|PA2
9	|PA1
10	|PA0
11	|B3
12	|B4
13	|E5
14	|E4
15	|B5
16	|Not Used
17	|E6
18	|B2
19	|B1
20	|F7
21	|F6
22	|F5
23	|F4
24	|F3
25	|F2
26	|F1
31	|F0
32	|E0
34	|E1
35	|D0
36	|C0
37	|D1
38	|C1
39	|D2
40	|C2
41	|D3
42	|C3
44	|D4
45	|C4
46	|D5
47	|C5
48	|D6
49	|C6
50	|D7
51	|C7
53	|Not used
54	|B0

If you're still having problems with dumping/checking/flashing your NOR/NAND. Google what problem you have, check the forums, and then post to a forum. There's a lot of forums out there and a lot of people who know this stuff so pick one you like.

## Hardware Problems
* PS3 Won't Turn On After Flashing
* YLOD
* Blank Screen After Installing QA toggle

If you patched to CFW, and it's firmware is higher then the firmware you were on, it might boot to a black screen or just turn off after 5 seconds, that’s normal. You just have to enter recovery.

* To boot into recovery mode turn your PS3 off. Now hold the power button until you get a beep, then a second beep and your PS3 will turn off.
* Press and hold the power button again until you get one beep, then a second beep and then let go of the power button. It should boot into recovery.
* Select “6. System Update” to reinstall the firmware.

If you got a blank screen after installing QA toggle then you have to remarry your blu-ray drive. baileyscream has a section on it as part of his [Ultimate Foolproof Downgrade Guide](http://www.ps3hax.net/showthread.php?t=39766), it's under all the colorful text.

### Things You Can Try
* Make sure it's plugged in and the power switch on it is in the ON position 
* Make sure you connected everything right when you put it back together, power connectors are fully seated, ribbon connectors connected all the way, power supply seated fully, fan plugged in, CMOS battery plugged in, hard drive installed.
* Make sure you didn't leave any bits of solder/wire/foreign objects in there.
* Something might have gone wrong with your patch or your flash. Try redumping the firmware on your PS3 and checking that it matches up with the patched one you wrote to it. You can use something like a md5 checker to quickly check if they're the same. If they don't match then re-flash the patched firmware to it.

# Troubleshooting the NORwegian Teensy Socket Edition

## Unknown Chip
If you get an unknown chip error this is usually because the socket isn't making good contact with the pins.

* Check to make sure all the pins on the NAND or NOR are straight and evenly spaced
* Check if the pins on the NAND or NOR sit completely flat, sometimes one will be higher or lower then the others
* Use a jewelers loupe/magnifying glass/microscope to line up the pins on the NAND or NOR with the pins in the socket
* Check Read Error section

## Read Errors / Dumps don't match
If the chip is recognized but your dumps don't match up or have lots of errors I've found power problems to usually be the cause.

* Make sure the 5v line on the Teensy is cut and that the 3.3V regulator on it is working (test for 3.3V at the 5V pin)
* If dumping a NAND try using external power
* You might have a "noisy" power supply, try adding a 10uF and a 100uF capacitor in parallel with your external power supply in order to try and mitigate the "noise".