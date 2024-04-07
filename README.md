# Custom-ZDoom-BehaviorTree
More sophisticated behavior in ZDoom actors with behavior trees.

This mod implements basic Behavior Tree management in ZScript in ZDoom; it's based on the [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI) and on my [https://github.com/StefanoP85/Custom-ZDoom-PathFinding].
The 3D model for the shield comes from [Lewisk3's HaloDoom](https://github.com/Lewisk3/HaloDoom_GZDoomVersion).
The NFG sprites and sounds come from the STRAIN.WAD from Alpha Dog Alliance, which inspired this mod.

## Features
The ZScript modules included in this repository contains the following functionalities:
* Multiple actions in the same tic frame (ex. moving and attacking)
* Multiple targets with a priority queue; the priorities are based on threat levels, obtained from the [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI)
* Some AI nodes, for repairing vehicles from [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI), and for medical staff

## Preview
In the following video, you may see some testing in the beautiful map Akzos City from Zanieon. (I cannot share the models and some AI nodes of their behavior are bound to the model's frames, so I could not include them in the mod.)

The scene depicts a friendly green/blue female Marine as a protagonist, and some red Doom Marines as antagonists.
* The first Doom Marine detects two opponents: me (the player) and the blue Marine; both of us are "white codes", so he starts attacking me, moving while attacking, but dies quickly after one shot from the blue Marine.
* The second (super) Doom Marine also detects us as both "white codes", so he also starts attacking me; when he's damaged by the blue Marine, she becomes a "green code" and hence the highest priority target of the red (evil) Marine; she destroyed him with some high damaging attacks, so she becomes a "yellow code".
* The third Doom Marine detects me as a "white code" and the blue Marine as a "yellow code", because my actors share these experiences as "Experienced threat level": he evaluates her as a dangerous opponent, and tries to attack her, but unsuccessfully.
* The fourth (super) Doom Marine follows the same decisions of the previous one, but fails too, raising the "Experienced threat level" of the blue Marine to "red code".
* The next two (super) Doom Marine detects me (the player) as a "white code" and the blue Marine as a "red code", becoming frightened and trying to escape the powerful opponent. The AI node of the actors are calling `KAI_MoveAway` from [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI).
* The last one is summoned behind the turns of the street, so he detects only me (the player), and immediately starts attacking, trying to following me. But when he spots the "red code" blue Marine, she becomes his highest priority target: he DID NOT stops shooting immediately, because the shooting behavior is encoded in the states, and much like the Chaingunners, Arachnotrons and Spider Masterminds, they may continue attacking, even if their target dies, because of random chance; so he actually fired some projectiles to the blue Marine, but starts immediately to an escape route. The red Marine tries to escape using `KAI_MoveAway` from [Inkoalawetrust's KAI library](https://github.com/inkoalawetrust/KAI), and the blue Marine follows him using `KAI_MoveTowards` and the NavMesh system.

[![Custom-ZDoom-BehaviorTree](https://img.youtube.com/vi/stvEKw8f2ds/0.jpg)](https://www.youtube.com/watch?v=stvEKw8f2ds "Custom ZDoom BehaviorTree")
