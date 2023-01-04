# Main Page
## Contents
- [MineTweaker3](https://minetweaker.github.io/wiki/Main_Page#:~:text=Planned%20Versions%20Credits-,MineTweaker%203,-Welcome%20to%20the)
- [Comparison with MineTweaker 2](https://minetweaker.github.io/wiki/Main_Page#:~:text=Mod%20Script%20Execution-,Comparison%20with%20MineTweaker%202,-Comparison%20with%20MineTweaker)
- [Tutorials (1.7.X)](https://minetweaker.github.io/wiki/Main_Page#:~:text=with%20MineTweaker%202-,Tutorials%20(1.7.X),-Lesson%201%3A%20Introduction)
- [Tutorials (1.6.4)](https://minetweaker.github.io/wiki/Main_Page#:~:text=Lesson%2010%3A%20Localization-,Tutorials%20(1.6.4),-Lesson%201%3A%20Introduction)
- [Guides](https://minetweaker.github.io/wiki/Main_Page#:~:text=Lesson%2010%3A%20Localization-,Guides,-Script%20Introduction%20Script)
- [Mod Support](https://minetweaker.github.io/wiki/Main_Page#:~:text=Expressions%20Script%20Functions-,Mod%20Support,-BetterStorage%3A%20BetterStorage%20Support)
- [Known Incompatibilities](https://minetweaker.github.io/wiki/Main_Page#:~:text=Additional%20Content%3A%20ContentTweaker-,Known%20Incompatibilities,-CraftingManager%20isn%E2%80%99t%20compatible)
- [References](https://minetweaker.github.io/wiki/Main_Page#:~:text=modifications%20are%20forbidden.-,References,-The%20following%20wiki)
- [Extending MineTweaker](https://minetweaker.github.io/wiki/Main_Page#:~:text=NBT%20Tag%20formats-,Extending%20MineTweaker,-More%20than%20ever)
- [Changelog & Planned Versions](https://minetweaker.github.io/wiki/Main_Page#:~:text=or%20contact%20me)-,Changelog%20%26%20Planned%20Versions,-Changelog%20Planned%20Versions)
- [Credits](https://minetweaker.github.io/wiki/Main_Page#:~:text=Changelog%20Planned%20Versions-,Credits,-Stan%20Hebben%2C%20as)


# MineTweaker 3
Welcome to the MineTweaker 3 wiki! The aim of MineTweaker is to provide modpack creators, server administrators and map makers with the capability of customizing Minecraft without having to write a custom mod for it.
All functionality is provided through an easy-to-use scripting language. (no prior knowledge or programming experience required!)

## Using MineTweaker, you can...
- Add and remove any crafting recipe
- Add and remove mod machine recipes for supported mods
- Modify the ore dictionary
Additionally, all scripts are sent from server to client, and thus only need to be stored server-side. They can be altered and reloaded without having to restart anything.

Forge Mods can also execute scripts in MineTweaker. [Mod Script Execution](https://minetweaker.github.io/wiki/mods/Mod_Script_Execution)

# Comparison with MineTweaker 2
[Comparison with MineTweaker 2](https://minetweaker.github.io/wiki/guide/Comparison_with_MineTweaker_2)

# Tutorials (1.7.X)
Lesson 1: Introduction
Lesson 2: Basic Recipes
Lesson 3: Ore Dictionary
Lesson 4: Furnace
Lesson 5: Advanced Recipes
Lesson 6: Item Renaming
Lesson 7: Tooltips
Lesson 8: Loot and seeds
Lesson 9: Loops
Lesson 10: Localization

# Tutorials (1.6.4)
Lesson 1: Introduction
Lesson 2: Basic Recipes
Lesson 3: Ore Dictionary
Lesson 4: Furnace
Lesson 5: Advanced Recipes
Lesson 6: Item Renaming
Lesson 7: Tooltips
Lesson 8: Loot and seeds
Lesson 9: Loops
Lesson 10: Localization

# Guides
Script Introduction
Script Statements
Script Expressions
Script Functions

# Mod Support
- [BetterStorage: BetterStorage Support]()
- [Blood Magic: Blood Magic Support]()
- [BuildCraft: BuildCraft Support]()
- [GregTech: GregTech Support]()
- [Harvest Festival: Harvest Festival Support]()
- [IC2: IC2 Support]()
- [Immersive Engineering: Immersive Engineering Support]()
- [Magneticraft: Magneticraft Support]()
- [MineFactory Reloaded: MFR Support]()
- [NEI: NEI Support]()
- [Tinkers' Steelworks: Tinkers' Steelworks Support]()
- [Witching Gadgets: Witching Gadgets Support]()
- [Additional Support: ModTweaker]()
- [Additional Content: ContentTweaker]()

# Known incompatibilities
- CraftingManager isn't compatible - crafting recipes can't load properly upon starting a game. (A manual reload does fix this, though, but it's not very practical)
- Some of the Sync recipes don't get modified properly. A manual reload fixes this. The issue is most likely due to Sync changing its own recipes depending on the server configuration, after MineTweaker did its work.
If you encounter any other incompatibilities, let me know, so I can add them to the list and save modpack authors a lot of time.

Although these mods should be compatible, it is not allowed to change RotaryCraft, ReactorCraft, ElectriCraft and ChromatiCraft recipes, or add recipes that modify the tech tree. The mod author, Reika, has explicitly stated that such modifications are forbidden.

# References
## The following wiki pages provide useful references:
- [NBT Tag formats]()

# Extending MineTweaker
More than ever before, you can extend MineTweaker with your own functionality.

## There are various things you can do:
- You can register global variables with minetweaker.MineTweakerAPI.registerGlobalSymbol(IZenSymbol). Use MineTweakerAPI.getJavaStaticGetterSymbol to get a static getter symbol or MineTweakerAPI.getJavaStaticFieldSymbol to get a static field symbol.
- You can register bracket handlers with minetweaker.MineTweakerAPI.registerBracketHandler(IBracketHandler). Bracket handlers can make it possible to create your own namespace for items/things in specific mods. See the minetweaker.mc17.brackets for example implementations.
- You can register custom classes with minetweaker.MineTweakerAPI.registerClass. Classes must have either a @ZenClass or @ZenExpansion annotation. Classes can be imported and called (handy for mod machines) and expansions can extend existing types (see minetweaker.data for examples, as well as minetweaker.item.IItemStack)
- In large projects, you can use the gradle RegisterZenClassesTask (see GitHub source in buildSrc) to generate a class containing a list of all registerable classes in your project. You can then submit the class name to MineTweakerAPI to make it register all those classes. All MineTweaker subproject use this system, so read those gradle build scripts to see how it's done. (or contact me)

# Changelog & Planned Versions
[Changelog]()
[Planned Versions]()

# Credits
- Stan Hebben, as mod creator.
- Jaredlll08 for helping Stan Hebben fix bugs and get that 1.8 version going!
- All those who reported bugs on GitHub, for otherwise I'd not be able to fix them.
- The beta testers: Ravin6666, Peach774, AnodeCathode, Dyonovan, Joshiejack
