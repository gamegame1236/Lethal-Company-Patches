# 2.0.4
+ Fixed issue with terminal always showing that purchasing slots is disabled in some cases.
+ Potential fix for other random issues. (sorry this is vague)
+ Checking if a reserved slot is unlocked is more accurate and fixes a few issues.
+ Still a lot more issues that I'm currently trying to consistently reproduce. Fixes will come soon!
+ If you have issues or bugs to share, I would appreciate if you could post an issue on the github, and let me know if you guys enabled purchasing slots in the config, who it affected, or was it everyone? Did it affect both host and clients? Can you reproduce it?<br>
Any of that information would be extremely helpful, and thanks!
# 2.0.3
+ Fixed terminal preventing the TooManyEmotes store from appearing.
+ Fixed some internal issues that was causing this mod to incorrectly identify an item in a reserved item slot.<br>
This is partially related to not being able to activate the flashlight with [F], or walkie with [X].
+ Disabled purchasing slots by default.
+ Terminal will now display under the Reserved Tip if the host disabled purchasing slots.
+ More fixes coming soon!
# 2.0.2
+ Fixed issue with non-host clients not unlocking slots when host disabled purchasing them.
+ Added pre-game reminder that reserved item slots won't be available until the round has started.
# 2.0.1
+ Quick fix for the terminal not showing tips related to this mod, or how to buy reserved item slots.
# 2.0.0
+ Re-did most (if not all) of the codebase revolving around reserved slots data, and how it is handled to support new features and API functionality.<br>
This update may break other mods' references to this one, and if so, I do apologize!
+ For more info regarding this update, please read the README.
+ Added progression. You can now purchase reserved item slots in the terminal! (can be disabled in the config)
+ Added API functions to offically allow mod developers to create their own reserved item slots, and add their items (any item) to it.<br>
The added API features also allows mod developers to easily add items from their mod (or even items from another mod) to existing reserved item slots, if this mod is enabled.
+ Even more configurable! The following config options can only be used if implemented by developers of reserved item slot mods.
+ Reserved item slot priorities can be can now be changed from their default values in the config.<br>
Changing priorities will change the order of the reserved item slots on the right (and left) side of your screen. The higher the priority, the further down in order they will be.
+ Adds support for adding extra items to reserved slots in the config.
+ Adds support for removing existing items from reserved slots in the config.
+ The ReservedItemSlotCore mod now handles all of the displaying of holstered reserved items. (Optional) When creating reserved items, or adding items to existing reserved item slots, mod developers can easily specify a bone to anchor a reserved item to when holstered, as well as a position/rotation offset.<br>
Read the README for more information on this.
+ The ReservedItemSlotCore mod now handles displaying reserved items on Masked Enemies, as long as developers define how their item will be displayed while holstered.
+ Added functionality to swap and toggle specific reserved item slots. Example: ReservedWeaponSlot has a keybind to toggle the reserved weapon slot. When pressed, that reserved slot will be toggled until you scroll off of it, without needing to hold Alt.<br>
This will need to be implemented by developers who create their own reserved item slot mods.
+ I probably broke a few things, or introduced new bugs with this update, so please post any major issues on my github. Thank you!
# 1.8.17
+ Fixed warnings when InputUtils is not enabled.
# 1.8.16
+ Re-restricted the use of this mod for non-host clients if the host does not have it enabled. This still CAN, and likely WILL cause desync issues if used this way, but for those who are stubborn enough, you can force allow this in the config. You have been warned!
# 1.8.15
+ Keybind display names should now display the correct keybind, whether on keyboard or controller.
+ All relevant keybind display names for this mod should automatically switch between keyboard and controller accordingly.
+ Added more controller support, with and without InputUtils. Works best with InputUtils installed, and easier to configure the controls.
# 1.8.14
+ Gave internal access to the ReservedKeySlot mod by: nitsuD
# 1.8.13
+ Revised a few methods to help prevent the error spam with players sending negative hotbar slot changes to the server.
+ Added more logs to help debug current or future errors.
+ Removed a block of code that could have been miscalculating the new reserved item slots start index when inventory size changes. (for other players)
+ As always, if this version seems unstable, please revert back to 1.8.12 until this has been updated.
# 1.8.12
+ Disabled adjusting inventory HUD elements in AdvancedCompany is enabled. (temporary maybe)
+ Small tweaks to code.
# 1.8.11
+ Added more reliable checks for the local player when the inventory size changes, for calculating which item slot index is the start of the reserved item slots. Should fix <i>some</i> issues.<br>
+ When using this mod with AdvanceCompany, (and it decides to behave itself) the reserved slots shouldn't use the feet slots from that mod.
+ If this mod creates errors with AdvancedCompany, it might be best to run without this mod (or AC) until the issue is fixed.
# 1.8.10
+ Minor changes.
# 1.8.9
+ Fixed some issues throwing errors in the console.
+ Fixed item appearing quickly and then disappearing from your hand when you pick up a reserved item.
+ Fixed control tips flickering to grabbed reserved item controls, and then back to the previous controls.
+ Maybe fixed more cases where you can't scroll in the reserved slots?
+ Added more code to support features for the reserved item slot mods.
# 1.8.8
+ Added more checks, and prevented some more issues if host does not have mod. (Again, use with caution!)
# 1.8.7
+ Fixed bug with controllers not being able to scroll through reserved hotbar slots with d-pad. (or another keybind)
+ Added some compatibility checks.
+ Reallowed use of reserved slot mods even if host doesn't have them. Use with caution!
+ Automatically changes any relevant control tooltips if player is using a controller or not.
# 1.8.6
+ Some compat tweaks.
+ Focus reserved hotbar tooltip now changes when keybind is updated in game. (with InputUtils)
# 1.8.5
+ Fixed the bug preventing you from swapping hotbars that I created in 1.8.4 (sorry!)
# 1.8.4
+ Removed old code that had methods being called before they were instantiated. Hopefully fixes some errors people are getting.
# 1.8.3
+ Fixed typo in bug.
+ Forgot to re-edit a line of code I changed that prevented the server from getting hotbar swap updates from the clients.
# 1.8.2
+ Fixed some bugs.
+ Added support for InputUtils, as a soft dependency. If this mod is enabled, you will be able to access any relevant hotkeys within the game's keybind menu. (will do the same for the individual reserved mods soon)
+ Added to the compatibility logic for other mods that increase inventory size. (may need more testing)
+ The reserved hotbar scroll direction should now match the mouse, regardless of inverted scroll settings.
+ (Readded) Swapping between reserved hotbar slots will now skip empty slots.
+ Attempted to refix compat with AdvancedCompany. May or may not work? No promises!
# 1.8.1
+ Added debug logs and dumps when errors occur when certain functions are called with incorrect values. Hopefully people share these with me on the Lethal Company Modding Discord!
# 1.8.0
+ Support for v47.
+ Slight code structure revamp.
+ Add compatibility between other mods that may change players' inventory size dynamically, such as LethalThings' utility belt. Not guaranteed for all mods.
+ Maybe added some bugs, idk.
# 1.7.7
+ Potential fix for the infamous de-sync issue.
# 1.7.6
+ Gave internal assembly access to LuckE's ReservedPersonalBoomboxSlot mod.
# 1.7.5
+ Tweaked more methods that could possibly cause de-sync.
# 1.7.4
+ More stability improvements and fixed more cases of potential de-sync issues. Probably still more to go, but should be at least a little more stable.
# 1.7.3
+ Added config entry to enable toggling swapping between the main hotbar slots and the reserved ones, rather than swapping while holding the hotkey.
+ Fixed quick bug with some reserved items being "registered" to the same reserved slot index amongst all clients. This will prevent some de-sync issues.
+ Reduced how often you can swap between the main and reserved hotbar slots. This will help with latency.
+ Will re-fix hotbar scroll direction in the reserved hotbar slots (up/down) to match scroll direction when I can ensure that it will sync with all clients, regardless of inverted values.
# 1.7.2
+ Fixed issue with clients not swapping their currently held reserved item correctly.
+ Restructured a part of this mod. Regardless of which of the reserved item slots that non-host clients have, they will now have all of the reserved item slots that the host is using, even if they don't have that specific mod installed.<br>
Syncing reserved slots from the host for a mod that you don't have should not cause any issues. You just won't have the extra features, such as any specific hotkeys for those mods, or items being displayed on players' while not currently held.<br>
This new adjusted framework can allow for custom reserved slots from the host to be synced with other clients, if I do end up making a CustomReservedItemSlot mod.
# 1.7.1
+ Fixed some compatibility issues in some cases with other mods not being able to run their transpiled code.
+ Scrolling up will now always scroll up in the reserved item slots.
+ Made swapping between reserved hotbar slots smarter. It will now not let you swap to empty inventory slots when focused on the reserved hotbar slots.<br>
There still may be syncing issues between which reserved item is held between players. Will update this next.
# 1.7.0
+ Added more tools for ReservedItemSlot mods.
+ Adds support for ReservedWeaponSlot!
# 1.6.7
+ Added support for ReservedSprayPaintSlot and the upcoming ReservedWeaponSlot mods.
# 1.6.6
+ My mod and LethalThings mutally broke compat with each other temporarily. Fixed now.<br>
My mod should now dynamically update the start index for the reserved slots in case other mods do change the order.
# 1.6.5
+ Temporary fix for reserved hud slots starting at index 4 regardless of hotbar size, when first joining a server.
# 1.6.4
+ Added support for other mods that might increase hotbar slots, such as LethalThings Utility Belt.<br>
# 1.6.2
+ Minor internal code tweaks.
# 1.6.1
+ Gave internal assembly access to LuckE's ReservedBoomboxSlot mod.
# 1.6.0
+ Revised structure of this mod.
# 1.5.2
+ Fixed issue with HUD not updating properly on custom inventory sizes. May not play well with other mods, aside from HotbarPlus that change inventory sizes.
# 1.5.1
+ Fixed invisible item issue when charging a reserved item.
# 1.5.0
+ Internal changes to support expanding inventory UI to keep the reserved item slots separate.
+ Should now support inventories that dynamically change in size. Adding inventory slots will copy the reserved item slots to the new last slots of the inventory, if needed.
# 1.4.4
+ Minor fixes.
# 1.4.3
+ Fixed (again?) being able to switch to your reserved hotbar while holding a two-handed item.
+ Improved logic for swapping between hotbars, or preventing you, while in certain animations or events.
+ Removed old debug logs.
# 1.4.2
+ Finally tracked down and fixed the bug preventing players from using their hotkeys to swap hotbars, or activate their reserved items with [F] or [X]
# 1.4.1
+ Fixed not properly handling PlayerActions in the OnDisable method if they were not yet initialized.
# 1.4.0
+ Major code restructure/organization to optimize network syncing and stability.<br>
Along with the restructure, more bugs and issues may be introduced, but these will be addressed asap!<br>
+ Reverted some functions to rely on built-in code to reduce the likelyhood of desyncs caused by these mods.<br>
This will help with future syncing with clients not uses these mods, but will likely not play nice with them at this point.
+ Other various fixes.
# 1.2.9
+ Fixed issue with being able to grab reserved items off of other players (caused de-sync)
# 1.2.8
+ Fixed issue where non-reserved items were going into the reserved item slots when the rest of the inventory is full.
+ Fixed a cursor tooltip issue showing that your inventory is full when looking at a ReservedItem, but you still have an available slot for it.
# 1.2.7
+ Fixed a few desync issues and tweaked some of the network transport settings.
+ Optimized some areas of code.
# 1.2.6
+ Fixed syncing issue with clients that occurs when clients leave and rejoin.
# 1.2.5
+ Swapping hotbar states should now be synced with all clients using this mod.<br>This means that the item held in each player's hand should be the same for everyone else.
# 1.2.4
+ Hopefully fixed all of the issues with grabbing and dropping reserved items, and a few other issues.
+ There are a few minor issues I ran into that I will fix soon.
# 1.2.2
+ Fixed issue with non-host clients not correctly picking up the ReservedItemSlot items.
# 1.2.1
+ Revamped functionality.
+ You can no longer swap to the reserved item hotbar slots, even if they're filled.
+ You can now swap to the reserved item hotbar slots by holding Alt, and scrolling up and down to switch between them.<br>
This way, you can swap to these items to drop them, as well as other actions, such as charging, storing, etc.<br>
The reserved item slots are still on the right side of the screen.
+ Added configs so you can change the swap hotbar modifier.
# 1.1.0
+ Reserved item slots now won't fade with the main hotbar.
# 1.0.0
+ Initial release