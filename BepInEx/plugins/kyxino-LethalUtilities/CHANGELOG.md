
<details open>
<summary>
<b>
1.2.x (LATEST)
</b>
</summary>

## 1.2.21 (Latest and FINAL until v2.0.0's rewrite!)
- Fixed some spawn weights not being adjusted when changed. (Naming was off from in-game and my code. Likely happened sometime after I was simplifying code post-v1.2.0.)

### 1.2.20 (IT'S THE FINAL BUG FIX!)
- In HUDSettings.cfg, fixed/changed my HideModListLC_API setting (under Clock Settings) to BlockPlayerModListLC_API (under HUD Settings). I was testing with LC_API v2.1.4, so I didn't realize that behavior was changed and that it didn't work, but now it is mostly fixed. It just shows the very first prompt when joining and that is it.
- I should hopefully be done breaking tiny features right away. I am setting things up for v2.0.0's rewrite, which will be better in every way.

### 1.2.19 (Even More Even More Bug Fixes Again Again Again Again!)
- Corrected JumpForce's default to 13 in CharacterSettings.cfg, forgot to test it, and Zeekerss loves changing defaults from what is shown.

### ~~1.2.18 (Even More Even More Bug Fixes Again Again Again!)~~
- Forgot to uncomment out some code for the spraypaint's volume setting, so I did that.
- Added an option to hide LC_API's mod list popup. (HUDSettings.cfg's ConfigEnabled + HideModListLC_API)
- Added an option to remove the game's jump delay. (CharacterSettings.cfg's ConfigEnabled + ApplyMovementModifiers + NoJumpDelay)
- Added JumpStaminaUse and JumpForce.

### 1.2.17 (Even More Even More Bug Fixes Again Again!)
- Fixed WeatherSetting's ScrapModifiersEnabled (if MapSetting's ScrapModifiersEnabled was off), I think I broke it in the previous update or so.

### ~~1.2.16 (Even More Even More Bug Fixes Again!)~~
- Added an option for skipping the boot animation, but not a full-on skip to online yet.
- Corrected SpawnModifiersEnabled/TimeModifiersEnabled.
- Fixed my "IT'S A BRAND NEW DAYYYYYYY." spam with TimeModifiersEnabled.

### 1.2.15 (More Even More Bug Fixes Again!)
- *Actually* fixed the funky teleporting issue when holding an item with the setting on.
- Fixed a bug in the game that uses my TimeSpeedScalar setting that basically caused the game to go out of sync with time.
- Fixed spraypaint no longer requiring to be shaked when GearSettings was in use.
- Prevented it from automatically changing settings if settings weren't changed. (For spraypaint.)
- Added a setting for the spray paint volume.
- Deprecated DayScalar in MapSettings. (Still works, just not recommended for supposed desync reasons?)
- Added LengthOfHours to MapSettings.
- Added NumberOfHours to MapSettings.
- ~~Added StartingGlobalTime to MapSettings.~~ ~~(Not enough time for testing.)~~ (Not used at all in the code, and can't be modified.)
- Separated some code and made more not run AT ALL if not enabled.

### 1.2.14 (Even More Bug Fixes Again!)
- Fixed FallDamage when set to false, now you won't take fall damage as said. It was funny finding out this was broken firsthand. (It no longer worked once v45 came out.)
- ACTUALLY fixed compatibility with Lategame Upgrades's Locksmith feature if you have KeysCanLockDoors on. (Previous update made things worse. You must lockpick every unlocked door. >:P)

### ~~1.2.13 (More Bug Fixes Again!)~~
- Fixed compatibility with Lategame Upgrades's Locksmith feature if you have KeysCanLockDoors on.
- Fixed time starting at 8:40ish when you had TimeModifiersEnabled on. (I accidentally switched the TimeSpeedScalar and DayScalar around probably back in v1.2.5.)

### 1.2.12 (Bug Fixes Again!)
- Fixed Lockpickers not being able to unlock doors when KeysCanLockDoors was enabled.
- Fixed Apparatus having additional multiplier applied when ScrapModifiersEnabled was on.
- *Likely* fixed items having their weight negated when teleporting with KeepItems.
- *Likely* fixed an issue with HotbarPlus.
- *Likely* fixed having to re-equip items after teleporting.
- Added my custom forked BepInEx.Configuration system to help with multiple things such as ordering. (May turn into an API soon.)
- MapSettings is now properly organized.
- Added my plugin metadata to every config because it is just good to do. (... and it can help with some things in the future.)
- Mod has been on a bit of a hiatus due to [CodeJoel](https://thunderstore.io/c/lethal-company/p/kyxino/CodeJoel/), [LethalEditor](https://thunderstore.io/c/lethal-company/p/kyxino/LethalEditor/), and [LethalModManager](https://thunderstore.io/c/lethal-company/p/kyxino/LethalModManager/), but I will be getting back to it big time again after I fully release [LethalModManager](https://thunderstore.io/c/lethal-company/p/kyxino/LethalModManager/).

### 1.2.11 (Added Discord Link)
- Added my new Discord to the Thunderstore page! (Haha, you thought this was a bug fix, it was actually a human fix because I forgot to do this in the previous version.)

### 1.2.10 (Last Bug Fix!)

- Fixed the global ScrapValueScalar's default not being the TRUE vanilla value of 0.4x.
- Fixed the global TimeSpeedScalar's default not being the TRUE vanilla value of 1.4x.
- You may need to adjust the above variables as they both used to be 1x.
- No more known bugs, LethalUtilities is now bug free! (I probably jinxed it!)

### 1.2.9 (More Bug Fixes!)

- Removed Min/MaxTotalScrapValue properties due to the game no longer using it.
- Fixed other interaction times being modified as well instead of just the Company bell.

### 1.2.8 (Teleporter Setting Fix)

- Fixed teleporting settings. Teleporters may behavior slightly different if it was misused.

### 1.2.7 (Bug Fixes)

- Did some small bug fixes, things shouldn't be too crazy now.

### 1.2.6 (New [README.md](https://thunderstore.io/c/lethal-company/p/kyxino/LethalUtilities/) Format)

- Made the README section look a lot nicer (after breaking it in 1.2.5, whoops.)

### 1.2.5 (Scrap Multiplier Fix)

- Fixed some scrap multipliers not undoing when switching maps/weather. + I'm working on a new mod/API that LU will use so that I'm not constantly accidentally messing things up as easily.

### 1.2.4 (Auto Offensive Value Fix)

- Fixed the auto Offense fix, it was really stupid.

### ~~1.2.3 (The Auto Fix That Needed a Fix in 1.2.4)~~

- Forgot that I should make it fix the old default values being set to 0 for Offense (along with some other things), so I did that, and now I have an excuse for 123.

### 1.2.2 (Fixed Offense Spawn Values)

- Fixed the issue with Offense having a bunch of values set to 0. I accidentally had the Company Building settings overwrite it.
- Changed when monster spawn weights apply, hopefully should apply any other mod so that they can overwrite my settings, if needed.
- Getting ready to change more variable names and make descriptions more pronounced.

### ~~1.2.1 (MapScalar Crash Fix)~~

- Added a cap to mapSizeMultiplier (aka MapScalar) to be capped at 1, otherwise crashes will likely happen.

## ~~1.2.0 (Major Map/Weather/Spawn Settings Update+More!)~~

- Reformatted the [CHANGELOG.md](https://thunderstore.io/c/lethal-company/p/kyxino/LethalUtilities/changelog/) to have the latest updates upwards rather than downwards.
- Fixed the mod version within the DLL, forgot to change it ever since v1.0.1, doesn't really change anything anyway.
- Automatically converting all other variables with part of their category names being prefixed into the individual variables. (Like the diff ConfigEnabled vars and map/weather settings.)
- Fixed the key door locking feature that didn't work unless both types of reuseable keys were enabled. (I think this happened during v1.1.2.)
- Got more than 5 hours of sleep 4 nights in a row.
- Huge map values customization.
- Added settings for monster spawn weights, INCLUDING MONSTERS FROM ANY MAP AND LASSO MAN.
- Added settings for the weather to change monster spawn weights. (Ex: Giants on Experimentation when Eclipsed... the struggle is real.)
- Added new items as gears for the TeleportSettings, along with new items coming out in LC soon.
- Added new settings for the new spray can item. (I will be updating sooner after the game updates next time, just was working on v1.2.0 for a while and stablizing it.)
- Adding proper time speed multipliers, DayScalar will remain around as it has a separate purpose, though confusing, I think it is just how far into the day you want to spawn along with actual time speed. TimeSpeedScalar will be the more obvious value for changing... well, the speed of time. Both can be paired together for better time results.
- Working on a new settings format for v2.0.0 that will be completely different and a LOT bigger/more expansive, which will allow for more additions even after this mod is outdated. (This may come out at the end of the month unless it gets too big, then I will likely have to turn it into a new mod entirely.)
- New teleporter setting for dropping everything but your held item and another for dropping everything that isn't gear and isn't your held item.
- Will be condensing the code to be better and more flexible.
- ~~Rename planets, change descriptions, risk levels (Next update, needs more testing to see if it is even stable.)~~ (I recommend LethalEditor for this in-depth customization.)

</details>
<details>
<summary>1.1.x</summary>

### 1.1.2 (The Light, I See the Light!)

- Made the [CHANGELOG.md](https://thunderstore.io/c/lethal-company/p/kyxino/LethalUtilities/changelog/) nicer looking to show all of my updates and idiocy.
- Forgot to re-add the config folder with the new changes.
- Also not entirely sure if the DLL properly applied in v1.1.1, so I confirmed it applied in this version.
- Goodnight, ladies and gentlemen, I will finally get some sleep. (Updates will no longer be rushed since the mod is already fulfilling its purpose of being able to edit a bunch of the games variables.)

### ~~1.1.1 (DLL might not have been updated, do not download.)~~

- Fixed [CHANGELOG.md](https://thunderstore.io/c/lethal-company/p/kyxino/LethalUtilities/changelog/) again... (Reminder, I'm getting sleep now.)

## 1.1.0 (DayScalar Update)</h2>

- Made things EXTREMELY compatible with other mods, so only if you have values changed from their default values will it actually apply ANY changes for that thing unless it is messes with another value that is modified that directly ties with it in the code.
- Fixed DayScalar (It was originally supposed to be removed, but I accidentally left it in along with code that errors MapMultipliers (and WeatherMultipliers if enabled) because of some config values I also removed, it was because it needed more testing, but I will leave it as it is until 1.2.0.)
- Readded my pre-release DayScalar values for each map.
- Added DayScalar per weather type. (You could make Eclipses long and insufferable, great idea, yes yes.)
- Fixed both [README.md](https://thunderstore.io/c/lethal-company/p/kyxino/LethalUtilities/) and [CHANGELOG.md](https://thunderstore.io/c/lethal-company/p/kyxino/LethalUtilities/changelog/) files to reflect recent changes.
- I'm getting more than 5 hours of sleep! (Greatest feature... starting today.)

</details>
<details>
<summary>1.0.x (NOT RECOMMENDED FOR DOWNLOAD.)</summary>

### ~~1.0.3 (Manual Instruction Fix)~~

- Fixed the Manual Installation instructions for the fixed config file structure. No redownload/update required.

### ~~1.0.2 (Default Config Fix)~~

- Fixed the default config files from being directly in the BepInEx/config folder, will now be in BepInEx/config/LethalUtilities upon download, I was sleep deprived and didn't see documentation, apologies for any inconveniences. Updates for v45 will be coming out soon.

### ~~1.0.1 (Config file discrepancy, do not download.)~~

- Moved all ConfigEnabled from ConfigSettings to each individual config for simplicity. It still won't execute any code other than the settings, which won't interfere with any mods.
- Also added the default config files so you don't have to load the game up first.

# 1.0.0 (Release)
Funnily enough, more stable than every version up to 1.1.1.

- Initial release.

</details>
