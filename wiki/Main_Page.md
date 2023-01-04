# Main Page
## Contents
[MineTweaker3]()
[Comparison with MineTweaker 2]()
[Tutorials (1.7.X)]()
[Tutorials (1.6.4)]()
[Guides]()
[Mod Support]()
[Known incompatibilities]()
[References]()
[Extending MineTweaker]()
[Changelog & Planned Versions]()
[Credits]()


# MineTweaker 3
Welcome to the MineTweaker 3 wiki! The aim of MineTweaker is to provide modpack creators, server administrators and map makers with the capability of customizing Minecraft without having to write a custom mod for it.
All functionality is provided through an easy-to-use scripting language. (no prior knowledge or programming experience required!)

Using MineTweaker, you can...
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
The following wiki pages provide useful references:
- [NBT Tag formats]()

# Extending MineTweaker
More than ever before, you can extend MineTweaker with your own functionality.

There are various things you can do:

You can register global variables with minetweaker.MineTweakerAPI.registerGlobalSymbol(IZenSymbol). Use MineTweakerAPI.getJavaStaticGetterSymbol to get a static getter symbol or MineTweakerAPI.getJavaStaticFieldSymbol to get a static field symbol.
You can register bracket handlers with minetweaker.MineTweakerAPI.registerBracketHandler(IBracketHandler). Bracket handlers can make it possible to create your own namespace for items/things in specific mods. See the minetweaker.mc17.brackets for example implementations.
You can register custom classes with minetweaker.MineTweakerAPI.registerClass. Classes must have either a @ZenClass or @ZenExpansion annotation. Classes can be imported and called (handy for mod machines) and expansions can extend existing types (see minetweaker.data for examples, as well as minetweaker.item.IItemStack)
In large projects, you can use the gradle RegisterZenClassesTask (see GitHub source in buildSrc) to generate a class containing a list of all registerable classes in your project. You can then submit the class name to MineTweakerAPI to make it register all those classes. All MineTweaker subproject use this system, so read those gradle build scripts to see how it's done. (or contact me)

# Changelog & Planned Versions
[Changelog]()
[Planned Versions]()

# Credits
- Stan Hebben, as mod creator.
- Jaredlll08 for helping Stan Hebben fix bugs and get that 1.8 version going!
- All those who reported bugs on GitHub, for otherwise I'd not be able to fix them.
- The beta testers: Ravin6666, Peach774, AnodeCathode, Dyonovan, Joshiejack
