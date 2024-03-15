# LethalUtilities
So much stuff that I don't know what ISN'T included here. You can reach me on Discord @kyxino (or my own Discord server at the top right) for help or the Lethal Company Modding community Discord in the top left.
## Overview
This is a mod that *can* do what a bunch of smaller mods can do, all changes are disabled, but can be selectively enabled, which makes it VERY ideal for modpacks. I got very annoyed with having over 20 individual mods doing 1 or 2 changes, so I decided to make a mod that can do a lot more than what those 20 mods can do, but keeping everything VERY vanilla, no actual revamping of any systems, which means it is unlikely for anything to break after the game updates.

## Manual Installation
1. [Setup BepInEx](https://www.youtube.com/watch?v=pefi48O-giU) (If not done already, video by *TheViperian* provided.)
2. Download and extract the latest version.
3. Place the folder *kyxino-LethalUtilities* in the *BepInEx/plugins* directory.
4. Run the game once for configs to load.
5. You can find the configs at *BepInEx/configs*, from there you can edit many different parameters of the game, but for them to apply/execute, you will have to enable each one using the ConfigEnabled value.
6. You can now launch the game. (Note: If playing with friends, they will need to install this mod and have the same settings as you for most of it to work properly.)

## Notice
**NOTHING IS CHANGED FROM THE BASE GAME, YOU MUST DO THE CHANGES IN THE CONFIGS YOURSELF, ANY CHANGES MAY INTERFERE WITH SIMILAR TASKED MODS.**
I will be adding many new features and allowing syncing between the host and players very soon, so just know ***everyone needs the exact same settings for now until I add syncing if you want it to work properly***. Config files are bound to change, but I have it in such a structure where it shouldn't undo any changes made by you for a while, so ***the config files will remain compatible until version 2.0.0 comes out later this month***. I may also make a Discord for this if enough people have downloaded this.

## Features
All are base game defaults, enable/change in configs. (THESE ARE DISABLED BY DEFAULT, SET ***ConfigEnabled*** TO APPLY CHANGES FOR EACH FILE AND ***\_ModifiersEnabled*** FOR EACH SECTION TO APPLY.)
- *GeneralSettings* (SaveItemCount- Allows you to raise the item count for saving.)
- *CharacterSettings* (Can enable/disable stamina and fall damage, along with different movement settings like walking, sprinting, climbing, and fast climbing.)
- *GearSettings* (Customize Spray Paint, Boombox, Key, Flashlights (normal and pro), and Walkie Talkies for inf use. Allow boombox to work when pocketed or disable when dropped. Allow key to lock doors.)
- *CompanySettings* (Can change the Company shopkeeper's hostility and make it always a full buying rate. Can change bell cooldown and selling wait time.)
- *MapSettings* (Customize scrap and monster spawning per map and globally along with map scale, day time scale, and time speed scale.)
- *WeatherSettings* (Customize scrap and monster spawning per weather type along with map scale, day time scale, and time speed scale.)
- *HUDSettings* (Change the clock to be or not to be viewed in the ship, outside, or the building, and in 24 hours.)
- *RoundSettings* (LoseScrapUponDeath, when everybody dies, you can choose to lose your scrap or not.)
- *LobbySettings* (Allow usernames with numbers and underscores or just any character in general. *Have not tested since I use letters like a cool person. 😎*)
- *ShipSettings* (CanOpenDoorInSpace, funny way to freak your friends out, cannot leave ship.)
- *TeleportSettings* (Allow keeping all items or just gear, along with cooldowns for each the regular and inverse teleporter.)

## Upcoming Features
- Server Host and Player Config Syncing
- In-game Customization Menu (Can save changes from in-game.)
- More specific item customization rather than the few inf settings.
- Menu skipping settings
- Quota settings, ship time, interaction time... pretty much anything that can be easily changed, I will be adding customization for, especially the ship door when landed.

## Known Issues
- Mod gets pretty funky if other players do not have the mod.
- Climbing will not have a scaled animation for faster speeds because of a lag issue until I fix it.
