# Changelog
## Contents
- [Version 3.0.10B](https://minetweaker.github.io/wiki/Changelog#:~:text=3.0.1%20Version%203.0.0-,Version%203.0.10B,-Temporarily%20disabled%20reload)
- [Version 3.0.10](https://minetweaker.github.io/wiki/Changelog#:~:text=.maxDamage%20%3D%20123%3B)-,Version%203.0.10,-Minecraft%201.8%20is)
- [Version 3.0.9C](https://minetweaker.github.io/wiki/Changelog#:~:text=if%20really%20necessary-,Version%203.0.9C,-Fixed%20removed%20recipe)
- [Version 3.0.9B](https://minetweaker.github.io/wiki/Changelog#:~:text=with%20BC%206.1-,Version%203.0.9B,-Fixed%20some%20wrongs)
- [Version 3.0.9](https://minetweaker.github.io/wiki/Changelog#:~:text=missing%20Harvester%20functions-,Version%203.0.9,-Added%20BuildCraft%20support)
- [Version 3.0.8B](https://minetweaker.github.io/wiki/Changelog#:~:text=generated%20from%20commands-,Version%203.0.8B,-Fixed%20furnace%20handler)
- [Version 3.0.8](https://minetweaker.github.io/wiki/Changelog#:~:text=on%20some%20mods.-,Version%203.0.8,-transformReplace%20now%20gives)
- [Version 3.0.7](https://minetweaker.github.io/wiki/Changelog#:~:text=entries%20in%201.7.10-,Version%203.0.7,-Added%20MFR%20support)
- [Version 3.0.6](https://minetweaker.github.io/wiki/Changelog#:~:text=be%20output%20properly-,Version%203.0.6,-Fixed%20a%20crash)
- [Version 3.0.5](https://minetweaker.github.io/wiki/Changelog#:~:text=the%20server%20console-,Version%203.0.5,-Fixed%20a%20couple)
- [Version 3.0.4](https://minetweaker.github.io/wiki/Changelog#:~:text=support%20to%201.7.2-,Version%203.0.4,-Fixes%20crash%20when)
- [Version 3.0.3](https://minetweaker.github.io/wiki/Changelog#:~:text=support%20for%201.6.4-,Version%203.0.3,-Finished%20IC2%20support)
- [Version 3.0.2](https://minetweaker.github.io/wiki/Changelog#:~:text=interface%20in%20general-,Version%203.0.2,-Added%20interface%20to)
- [Version 3.0.1](https://minetweaker.github.io/wiki/Changelog#:~:text=clients%20in%201.6.4-,Version%203.0.1,-Secured%20the%20in)
- [Version 3.0.0](https://minetweaker.github.io/wiki/Changelog#:~:text=bugs%2C%20/mt%20forum)-,Version%203.0.0,-Initial%20release.)


# Version 3.0.10B
Temporarily disabled reload checks as they caused trouble
Fixed recipes not reloading on servers, sometimes (thanks to mrammy)
Can now set max damage (<myitem>.maxDamage = 123;)
# Version 3.0.10
Minecraft 1.8 is now supported!
Support for 1.6.4 and 1.7.2 has been dropped.
Retired GregTech support. This has been superseded by the GT5 addon by DreamMasterXXL.
You can now set block hardness and maximum stack size. (<item>.hardness = 123; <item>.maxStackSize=4;)
Fixed /mt help being broken in some cases
Fixed the tools.jar not being found automatically (credits to RX-14)
Fixed /mt hand crashing in some cases
Fixed usage of quotes when setting names
Fixed MFR Safari net integration
Fixed MFR Fertilizer integration
game.lock() can now be used to prevent reloading. Will show an error screen if reload was necessary
Reloading of scripts is now only performed if really necessary
# Version 3.0.9C
Fixed removed recipe rollback being broken in some rare occurrences
Temporarily disabled support for BuildCraft 6.1 . This fixes a crash on startup with BC 6.1
# Version 3.0.9B
Fixed some wrongs in data matching, causing crashes with onlyWithTag in some cases
Fixed a variable check when resolving variables (caused a crash)
Fixed multiple saplings with the same ID not working in the Planter
Fixed crash when using /mt hand on a dedicated server
Fixed crash in /mt recipes in some cases
Added a couple missing Harvester functions
# Version 3.0.9
Added BuildCraft support
Improved exception handling; exceptions that break scripts will now log to the minetweaker log for better bugfixing
/mt hand now copies to the clipboard
/mt hand now also outputs the oredict entries it is in
Added /mt recipes command
Added /mt recipes hand command
Can now properly add strings and formatted strings
Removed COMMAND: in the minetweaker.log file in front of lines generated from commands
# Version 3.0.8B
Fixed furnace handler crashing in 1.7 on some mods.
# Version 3.0.8
transformReplace now gives the replacement item in the player inventory if it is port of a stack (instead of modifying the whole stack)
Added noReturn transformation to avoid any item from being returned. Suppresses programmed vanilla/mod behavior to, for example, given a bucket back.
Added giveBack() and giveBack(item) transformation to return the item, or a replacement item, back into the inventory instead of the crafting table. Fixes fighting between transformations and default mod/vanilla behavior.
Added tooltip support. Includes formatted tooltips.
Added ability for mods to execute MineTweaker scripts via IMC messages
Ported chest loot modification from ModTweaker
Ported setLocatization from ModTweaker
Added dev builds
Fixed asterisks in multiline comments breaking script parsing.
Fixed removeShaped function not working properly if no ingredients are given.
Fixed addAll for oredict entries in 1.7.10
# Version 3.0.7
Added MFR support for 1.6.4 and 1.7.10 (not all machines and documentation is finished yet)
Added /mt entities command to see all registered entities
Added /mt biomes command to see all biomes in the game
Added mirrored shaped recipes
Can now make recipes work only in a specific game mode
Can now make simple function recipes
Fixed spaces in item names
Added block info command. Gives information about blocks you are clicking on
Mods can now use the onReload function to execute certain actions upon reload
NBT compound tags with non-identifier keys should now be output properly
# Version 3.0.6
Fixed a crash when using minetweaker commands from the server console
# Version 3.0.5
Fixed a couple GregTech machines
Expanded GregTech support to 1.7.2
# Version 3.0.4
Fixes crash when opening DartCraft clipboard
Added GregTech support for 1.6.4
# Version 3.0.3
Finished IC2 support (and extended it to 1.6.4)
Extended NEI support to 1.7.10
Fixed crash upon startup in 1.7.10
Can now craft with IC2 tools and have it consume energy upon crafting
Fixed 1.7.10 chat messages resulting in a stack overflow
3.0.3B: fixed 1.7.10 not being built properly, causing items not to be resolved and breaking the entire API interface in general
# Version 3.0.2
Added interface to game, client and server
Added transformations
Made ingredient conditions more practical to use, no longer requires imports
Started implementation of event handling
Moved commands and logic to the common API code
Added common interface to MineTweaker recipes
Added string methods
Moved the logger from static value to static getter
Fixed crashes on dedicated servers
Fixed bracket resolution for <id:meta> values in 1.6.4
Fixed scripts not being sent to multiplayer clients in 1.6.4
# Version 3.0.1
Secured the in-game minetweaker command to be op-only
Can now open wiki, bugs and forum from the /mt command (/mt wiki, /mt bugs, /mt forum)
# Version 3.0.0
Initial release.