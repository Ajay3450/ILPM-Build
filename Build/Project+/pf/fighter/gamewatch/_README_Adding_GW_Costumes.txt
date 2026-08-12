=======================================================================================
Guide for Game and Watch Costumes
=======================================================================================

A number of changes were made for Game and Watch costume files to support alternate costumes.

Costumes 00 - 19 will use FitGameWatch00 (Default)
Costumes 20 - 29 will use FitGameWatch01 (Judge)
Costumes 30 - 39 will use FitGameWatch02
Costumes 40 and onward will use FitGameWatch03

If you wish to adjust these ranges for further customization, see the code Project+\Source\LegacyTE\LoadFlags.asm

=======================================================================================
Adding Game and Watch Recolors
=======================================================================================
Game and Watch recolors are set through the Animation Data[10] and Animation Data [0] [Group 1] CLR entries in each pac.

You can edit the ColorRegister0 in each to select the base color and outline.

Do not use costume slots 12 and 13, they are colored bright red and will not work.

=======================================================================================
EntryFile
=======================================================================================
FitGameWatchEntry.pac, a file loaded from the Brawl disc was disabled, because coding separate entry files for alternate costumes is not currently possible.

=======================================================================================
AdditionalBones and Vis0
=======================================================================================
For anyone making new Game and Watch alternate costumes, or adding existing Game and Watch alternate costumes that were not built with P+ in mind, there are some additional bones.

Be sure to make all of these new bones Visibile as False, if adding to a pre-existing costume.

Bone 98 - HeadFront: Used for when Game and Watch faces the front, can be used to get specific looks from the front vs the side. For any new costume creators, be sure to test HeadFront, and all the Vis0 animations in FitGameWatchMotionEtc that call it.

Bones 99 - 103: Entry1, Entry2, Entry3, Entry 4: These bones replace the entry file, and are set up based on the frames of Game and Watch's entry animation. The entry objects in FitGameWatch01 are the easest way to set this up, and new costume creators should review them in their modelling software of choice.

