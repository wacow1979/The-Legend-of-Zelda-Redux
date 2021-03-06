# THE LEGEND OF ZELDA REDUX

-------------------

# **Index**

* [**The Legend of Zelda Redux Info**](#the-legend-of-zelda-redux)

* [**Changelog**](#changelog)

* [**Optional Patches**](#optional-patches)

* [**Help needed for these points**](#help-needed-for-these-points)

* [**Patching and Usage Instructions**](#instructions)

* [**Credits**](#credits)

* [**Project Licence**](#license)


-------------------

## The Legend of Zelda Redux

Continuing over from the Zelda II Redux hack, The Legend of Zelda Redux aims to tackle some of the odd design and programming decisions from the original NES classic to revitalize and give new life to the beloved and cherish classic.

This hack tries to address a lot of points to make the game fit with the rest of the series (and Zelda 2 Redux) by doing some rebalancing and QoL changes, and also some visual flare into the game, without compromising the original game's design. Be sure to check the full Changelog inside the ReadMe file for the full list of changes made to this hack, and also don't forget to check the optional patches too!

Want to see the full development of the hack?

Follow it on the Romhacking.net thread:
https://www.romhacking.net/forum/index.php?topic=29403.0


-------------------

## Changelog

* **[DONE]** Save manually with Up+A when in the Items Subscreen
* **[DONE]** Reworked heart HUD to match Zelda 2 Redux
* **[DONE]** Relocalization of the  game's script to better match the Japanese release, or have better hints altogether. Based on the Legends of Localization book/webpage (Except the two iconic "Take this" and "It's a secret" lines)
* **[DONE]** Make the Blue tunic more vibrant
* **[DONE]** Increment the initial bomb max. amount to 10 instead of 8
* **[DONE]** Increment the bomb upgrades by 10 instead of the original 4. First upgrade should give you 20 bombs, second will be 30.
* **[DONE]** Faster text printing
* **[DONE]** Modify the Sword beam to only be active when at full health/heart, and stop shooting when the life gets to 3/4 of a heart
* **[DONE]** Modify certain item names to better match subsequent official names in the franchise (Rupee, Fairy, Heart Container, etc.)
* **[DONE]** Change the Red and Blue rings to Red and Blue tunics
* **[DONE]** Introduction text rewrite
* **[DONE]** Reimplementation of the warning screen from version PRG1 upon Game Over / Saving
* **[DONE]** Slight modifications to the title screen to give the "ZELDA" title a red colour (modified fading palettes to match this change too)
* **[DONE]** Possibly also add a breakable tile hint for overworld tiles
* **[DONE]** Automap Plus, but modify it to have 1/4 heart decrements instead of 1/8 (this is needed in order to make space in sprite PPU for the next point (#3)
* **[DONE]** Visible hint for breakable walls in Dungeons (already implemented, just need sprite space for the left walls)
* **[DONE]** Remove the 1 Rupee flashing, and make it green if possible
* **[DONE]** Press the Select button to toggle the item selected for the B Button (to avoid pausing the game to select an item everytime)
* **[DONE]** Change the duplicate bosses in Level 4 and 7 (Gleeok and Aquamentus) to Lanmola and Patra respectively.
* **[DONE]** Have 999 rupees as the maximum amount, instead of 255. The rupee amount also needs to be saved in SRAM for when the game loads, so it starts with whatever amount you had last time (thanks to Bogaa for this feature!)
* **[DONE]** Add a proper arrow enemy-drop item and an arrow counter (shops give 30 arrows when purchased), with the max arrow limit being 30 for normal Arrows, and 60 once you get the silver Arrows (thanks to Bogaa for the Arrow drop/counter code, and stratoform for the Max arrows limits!)
* **[DONE]** Slight graphic changes to make certain sprites match their official artwork (Link now has his yellow hat line, some shield slight change, etc.). This won't be a graphic update of the game, as I still want to retain the original game's overall art design and aesthetic, but with sprites that better depict their official artwork designs.
* **[DONE]** Be able to kill the Pols Voice by playing the flute, and also with arrows to retain the original way of killing them (Thanks to stratoform for this!)
* **[DONE]** Flip the heart rows in the File Select Screen (Thanks again stratoform!)
* **[DONE]** 

* Save the amount of hearts you last had if the game was saved manually, so when you load, you start with the same amount of life (this I'm not sure if it will be implemented in the end hack)
* Implementation of a Copy/Erase file system like in subsequent Zeldas, where D-Pad Up and Down control the cursor in the File Selection and pressing A brings up the Name screen (Example: ALttP)
* Animated tiles for water (maybe bushes). Perhaps this could be done by converting the ROM to something like MMC3/MMC5 for bank switching
* Diagonal sword swing

-------------------

## Optional patches:

* Modify bomb upgrade amount to 05 per upgrade (Bomb Upgrades 5 instead of 10.ips)
* Link's Awakening graphics patch (Link's Awakening GFX.ips)
* Original NES graphics (Original NES GFX.ips)
* Unique bosses in each Dungeon/Level (Rearranged Bosses.ips)
* Make each dungeon have its own unique colour palette similar to Modern Classic Edition (Recoloured Dungeons.ips)

-------------------

## Help needed for these points:

* Implementation of a Copy/Erase file system like in subsequent Zeldas, where D-Pad Up and Down control the cursor in the File Selection and pressing A brings up the Name screen (Example: ALttP)
* Animated tiles for water (conversion to MMC5 for bank switch?)
* Diagonal sword swing


-------------------

## Instructions

To play The Legend of Zelda Redux, the following is required:

* FCEUX 2.2.3 or above
* The Legend of Zelda NES ROM (Legend of Zelda, The (USA).nes, MD5: 337bd6f1a1163df31bf2633665589ab0)
* Lunar IPS
* Zelda1_Redux.ips patch

Grab the patches from inside the /patches/ folder from the GitHub page, or alternatively, download the .zip file from the Releases page (once a proper release is out) and apply the patch over your Legend of Zelda ROM with Lunar IPS.
If you want to apply any of the optional patches, you can use each Optional patch individually from inside the /patches/optional folder depending on your liking over your already patched The Legend of Zelda Redux ROM, or you can either compile them manually from the source code, although this is not recommended if you are not familiar with compilations or 6502 assembly.

-------------------

## Credits

* **Trax** - For his amazing disassembly of Zelda 1, which helped with a ton of stuff, and also for a lot of feedback and help in the development of this hack.
* **BogaaBogaa** - For his incredible help with the Arrows and 999 rupees code, and with flipping the Heart/Map positions in the HUD
* **DarkSamus993** - For his ASM help towards some hacks (like the Select button Item switch)
* **Stratoform** - For his help and code towards the Pols Voice flute code, fixing both the remaining stuff from porting the PRG1 Game Over screen's flashing and the cracked overworld walls collision, the flip hearts code and the max arrow limits
* **snarfblam** - For the Automap hack, which was disassembled and modified to work with 1/4 hearts instead of 1/8 exclusively for this project
* **gzip** - For his Select button fix and the slow waterfall animation
* **abw** - For the code cleanup and optimization on Bank 6 that made the repointing of the "LEVEL-X" text possible
* **lexluthermeister** - For his help on creating the Optional patch for the new bosses
* All other users that gave their feedback on possible ways to improve the game over at the [RomHacking.net](https://www.romhacking.net/forum/index.php?topic=29403.0) thread, and those that gave insightful ideas and mockups!

-------------------


## License

The Legend of Zelda Redux is a project licensed under the terms of the GPLv3, which means that you are given legal permission to copy, distribute and/or modify this project, as long as:

1) The source for the available modified project is shared and also available to the public without exception.
2) The modified project subjects itself different naming convention, to differentiate it from the main and licensed The Legend of Zelda Redux project.

You can find a copy of the license in the LICENSE file.
