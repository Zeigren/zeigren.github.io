---
layout: post
title:  "PS3 Downgrading PS3 Teardown"
excerpt: "Taking Apart Your PS3"
ps3guide: true
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

Here is a list of all the different motherboard revisions on [psdevwiki.com](http://www.psdevwiki.com/ps3/Motherboard_Revisions).

I've taken pictures of the downgradable motherboards from there, and annotated them with their NAND/NOR locations.

## COK - 001
![COK-001_BOTTOM](/assets/img/COK-001_BOTTOM.jpg){:class="img-responsive"}
![COK-001_TOP](/assets/img/COK-001_TOP.jpg){:class="img-responsive"}

## COK-002/COK-002w
![COK-002_TOP](/assets/img/COK-002_TOP.jpg){:class="img-responsive"}

## SEM-001
![SEM-001_Topside](/assets/img/SEM-001_Topside.jpg){:class="img-responsive"}
![SEM-001_Bottomside](/assets/img/SEM-001_Bottomside.jpg){:class="img-responsive"}

## DIA-001
![DIA-001_TOP](/assets/img/DIA-001_TOP.jpg){:class="img-responsive"}

## DIA-002
![DIA-002_TOP](/assets/img/DIA-002_TOP.jpg){:class="img-responsive"}

## VER-001
![VER-001-TOP](/assets/img/VER-001-TOP.jpg){:class="img-responsive"}

## DYN-001
![DYN-001_TOP](/assets/img/DYN-001_TOP.jpg){:class="img-responsive"}

## SUR-001
![SUR-001_TOP](/assets/img/SUR-001_TOP.jpg){:class="img-responsive"}

## JTP-001/JSD-001
![JTP-001_TOP](/assets/img/JTP-001_TOP.jpg){:class="img-responsive"}

NORs have only one NOR.

NANDs have two NANDs. Both need to be dumped and then flashed to again. There's NAND0/LOW and NAND1/HIGH, you can see which is which in the pictures above.

# [Setting Up The Clip Edition Continue - Page 4a]({{ "/PS3-Downgrading-Setting-Up-The-Clip-Edition/" | relative_url}})

# [Setting Up The Socket Edition Continue - Page 4b]({{ "/PS3-Downgrading-Setting-Up-The-Socket-Edition/" | relative_url}})
# [Troubleshooting]({{ "/PS3-Downgrading-Troubleshooting/" | relative_url}})