---
layout: post
title:  "PS3 Downgrading PS3 Teardown"
excerpt: "Taking Apart Your PS3"
guide: true
tag:
- Guide
- PS3 Downgrade
- PS3 Teardown
comments: false
---
# Take Apart PS3
Here's a guide for taking apart a [Fat PS3](https://www.ifixit.com/Teardown/PlayStation+3+Teardown/1260) and one for a [Slim PS3](https://www.ifixit.com/Teardown/PlayStation+3+Slim+Teardown/1121)


You'll need the motherboard without anything attached to it. 
You don't need to take the fan out of the heatsink assembly. 
I recommend using something like an ice cube tray to put screws in.
Use a different cube for each layer you take apart. 
One cube for the outside screws, one cube for the screws that go on the top side of the motherboard, etc...


# Find The Chip
Now we need to find the NOR or NAND on the motherboard. 
Since there are so many different motherboard revisions there are a lot of places the NAND or NOR could be located.

Here is a list of all the different [motherboard revisions](http://www.psdevwiki.com/ps3/Motherboard_Revisions)

You can check that site and see the name of the NAND or NOR Flash Storage on your motherboard. 
Which can help you find it on your board (like COK-001 has Samsung K9F1G08U0A-PIB0 NANDs).

Also just google your board revision plus NAND or NOR to find pictures of where it's located. I'll probably upload some here at some point.

NORs have only one NOR.

NANDs have two NANDs. Both need to be dumped and then flashed to again. There's NAND0/LOW and NAND1/HIGH. Unfortunately they're in different places depending on the board so here's a list of which is which. Lifted from psdevwiki.com.

```
COK-001 :
IC3802 LOW (main componentside next to Starship2)
IC3803 HIGH (backside next to 60-pin BD ATA connector)
COK-002 + COK-002W :
IC3802 LOW (main componentside between SATA connector and South Bridge)
IC3803 HIGH (main componentside between SATA connector and AV Multi connector)
SEM-001 :
IC3802 LOW (backside)
IC3803 HIGH (main componentside with SATA connector, CELL BE, RSX etc.)
```

# [Setting Up The Clip Edition Continue - Page 4a]({{ "/PS3-Downgrading-Setting-Up-The-Clip-Edition/" | relative_url}})

# [Setting Up The Socket Edition Continue - Page 4b]({{ "/PS3-Downgrading-Setting-Up-The-Socket-Edition/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})