# Custom-ZDoom-BehaviorTree
More sophisticated behavior in ZDoom actors with behavior trees.

This mod implements basic Behavior Tree management in ZScript in ZDoom; it's based on the [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI) and on my [https://github.com/StefanoP85/Custom-ZDoom-PathFinding].
The NFG sprites and sounds come from the STRAIN.WAD from Alpha Dog Alliance, which inspired this mod.

## Features
The ZScript modules included in this repository contains the following functionalities:
* Multiple actions in the same tic frame (ex. moving and attacking)
* Multiple targets with a priority queue; the priorities are based on threat levels, obtained from the [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI)
* Some AI nodes, for repairing vehicles from [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI), and for medical staff
