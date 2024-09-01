# Custom-ZDoom-BehaviorTree
More sophisticated behavior in ZDoom actors with behavior trees.

This mod implements basic Behavior Tree management in ZScript in ZDoom; it's based on the [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI) and on my [navmesh system](https://github.com/StefanoP85/Custom-ZDoom-PathFinding).

## Features
The ZScript modules included in this repository contains the following functionalities:
* Multiple actions in the same tic frame (ex. moving and attacking)
* Multiple targets with a priority queue; the priorities are based on threat levels, obtained from the [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI)
* Some AI nodes, for repairing vehicles from [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI), and for medical staff

## Credits

### Sounds
The Shield effects sounds come mostly from HaloDoom and some other sounds are made by me, by editing sounds from Freesound.org.
The NFG sounds (and sprites) come from the STRAIN.WAD from Alpha Dog Alliance, which inspired this mod.
The other weapons sounds are made by me, by editing sounds from Freesound.org. 

### Sprites
The ARM0* sprites are made by me; BAL5* & BAL6* comes from the Shareware version of Doom by ID Software.
The BAT* & NFG* sprites and sounds come from the STRAIN.WAD from Alpha Dog Alliance, which inspired this mod.
The PUL* sprites come from ID Software, ShadesMaster.

### Models
The Lightning gun model comes from the Hunter's Moon project and the idea of the weapon come from [Jekyllgrim's ZSLightningGun](https://github.com/jekyllgrim/ZSLightningGun)
