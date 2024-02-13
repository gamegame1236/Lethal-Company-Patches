# LateGameUpgrades
***INSTALL THE DEPENDENCIES***  
***ALL CLIENTS NEED THIS MOD INSTALLED***  
to install just put the MoreShipUpgrades folder in your BepInEx plugins folder.

### *Everything about this mod can be changed via the extremely extensive config "com.malco.lethalcompany.moreshipupgrades.config"*  
The hosts config is automatically synced from host to remote clients.
200+ config options allows the mod to fit anyone's playstyle.

Type `lategame` in the terminal to see mod info!  
Type `lategame store` or `lgu` to view current upgrade status and cost.  
Type `info <upgrade>` for dynamic info.

This adds:
- 20 upgrades.
- 5 complex team oriented missions (contracts).
- mission items, npc, rewards, and behaviours.
- 8 new store items.
- 1 rare scrap (shopping cart).

The goal of this mod is to allow you to make playthroughs last longer and to remedy the stale lategame of not having anything to spend your money on and only going to one moon.

If using V40 - downgrade to V2.1.0  
If using v45 - downgrade to v2.8.6

## V 3.1.1
Fixes
- Intern command is fixed now.
- Fixed Back Muscles exploit prevention clamp not applying and allowing negative weight values.
- Fixed Load LGU command not working when there are non-null player controllers with null attributes.
- Wheelbarrow configurable price was using the night vision configurable price before.
- Probably a couple more wheelbarrow fixes.

## V 3.1.0
Additions
- Shutter Batteries Upgrade
    - Increase the amount of time the doors stay closed.
- Scrap Insurace
    - Insure the scrap in your ship for your next moon visit.
- Contracts can be purchased for specific moons for an increased price.
- Press middlemouse button to drop all items in a wheelbarrow.

Changes
- Contract object spawn location fixes.
    - Contract objects now spawn one unit forward of enemy vents.
    - This will prevent contract objects from spawning in unreachable areas or in walls.
    - Additionally this will provide balance to objects spawning too close to the entrance sometimes.
    - By default they will spawn at the vent furthest from the entrance but can be configured to spawn at a random vent.
- Available contracts can be removed via the config.
- Lightning rod now makes it so power doesn't go out when ship is struck.
- Can no longer do the same contract twice.
- Misc section in config is now `_Misc_` so it shows at the top of the file. If you don't delete your config you will still have the old `Misc` section that won't do anything.
- Scrap Wheelbarrow rarity value has been inverted to be more intuitive. It's now 0.1 by default (10%). If you have your old config it will be 0.9 (now 90%)!
- Contracts now support modded moons.
- Better descriptions have been added to the config for shared upgrades.

Fixes
- Wheelbarrow global sound and behaviours fixed.
- Some contract details not syncing to remote clients properly.
- Exorcism failure missing a failure step on some moons.
- Active contract not going away has been fixed.
- Dropping an item on a pentagram instead of placing it will no longer make it irretrievable.
- Fix locksmith not working after loading save.
- Fix sick beats from not loading in save.
- Enable wheelbarrow = false fix.
- Particle effects on samples not disabling.

*That's all that's coming to mind but there's probably a more I'm forgetting*

## V 3.0.4
Fixed ritual site sync (scan node and item placement), wheelbarrow weight calculation, data pc local user input, bruteforce command vanilla integer overflow, demonic tome value, multiple contract objects appearing if lobby was recreated, more probably

entering `contract` when you already have a contract now also displays the `info contract` message.

lowered volume of extraction scavenger, added config option for volume for extraction scavenger (set to 0 to mute, still attracts enemies), increased interval between voice clips for extraction scavenger, and if he is inside the ship his voice clip interval is trippled. Should make him a little less annoying.

## V 3.0.3
More fixes, Data PC contract object not working on remote client, wheelbarrow polish, more

Bugs being worked on: Bomb can spawn kind of inside the wall and be impossible to defuse / read serial code. Apparently multiple contract objects can spawn? EX: 3 scavengers to extract will spawn.

## V 3.0.2
Just some bug fixes, most importantly not being able to move after dying lol.

Additionally issues with disabling items in the config should be resolved.

Wheelbarrows, shopping carts, and the scavenger you rescue in the extraction contract aren't being saved by the ship at the moment even though they should be. Being investigated but we're both off for the night so I thought I'd get this out first.

## V 3.0.0
*This is probably my favourite update so far and should breathe a lot of life into the game.*
### Contracts
Contracts are difficult team oriented missions that serve two purposes: extra income and incentive to visit non high tier moons.  
Enter contract into the terminal to receive a random contract for a random moon.  
*As usual all contracts are completely configurable.*  
Currently there are 5 contracts implemented (click to expand):
<Details>
  <summary><b>Exorcism Contract</b></summary>
    <ul>
      <li>Paranormal activity has been detected in the facility at the given moon.</li>
      <li>You must find the ritual site, discover what type of ghost you have to exorcise, enter `demon GhostType` into the terminal to get the correct ritual instructions.</li>
      <li>Collect ritual items and correctly conduct the ritual to banish the ghost and get your loot.</li>
      <li><Details><summary>Click for consequences of failure spoiler</summary>A satanic chant will start, the site will explode, and ghost girls will spawn on the site.</Details></li>
      <li>10 ghost types</li>
      <li>5 ritual items</li>
    </ul>
</Details>
<Details>
  <summary><b>Data Contract</b></summary>
    <ul>
      <li>An active device has been detected in the facility at the given moon.</li>
      <li>You must find it then 'hack' it and retrieve a valuable .db file.</li>
      <li>To do this you have to enter the devices IP address into the terminal with the bruteforce command.</li>
      <li>Then you can login with the credentials and start looking for the file through the terminal.</li>
      <li>use `ls` `cd` and `mv` ls lists the files in that directory, cd changes to a directory (.. or ~ to go back) and mv moves a file (use to win the game).</li>
      <li>EX: `cd someDirectory`, `cd ..`/`cd ~`, `ls`, `mv survey.db`</li>
    </ul>
</Details>
<Details>
  <summary><b>Exterminator Contract</b></summary>
    <ul>
      <li>The facility at the given moon has become overun with Hoarding bugs.</li>
      <li>You must find and destroy their nest.</li>
      <li>The bugs are very aggressive. Work tactifully with your team to ensure your success.</li>
      <li>Hold E on the nest to destroy it and get the loot.</li>
      <li>Pair with the hunter upgrade to get filthy rich.</li>
    </ul>
</Details>
<Details>
  <summary><b>Bomb Defusal Contract</b></summary>
    <ul>
      <li>A bomb has been planted in the facility at the given moon.</li>
      <li>You must locate and defuse it.</li>
      <li>Each bomb will have three wires, a timer, and a serial number.</li>
      <li>Enter `lookup SerialNumber` in the terminal to get defusal instructions.</li>
      <li>Cutting the wrong wire is fatal, entering the wrong serial number will give you incorrect instructions.</li>
    </ul>
</Details>
<Details>
  <summary><b>Extraction Contract</b></summary>
    <ul>
      <li>An operative from another crew has been lost in the facility on the given moon.</li>
      <li>You must find and retrieve them.</li>
      <li>You will need to bring or find a medkit to heal them then carry them out.</li>
      <li>Animated NPC with 20 custom voicelines and 3 different states.</li>
      <li>Very loud.</li>
    </ul>
</Details>

### Items / Upgrades
- Helmet
    - Blocks incoming damage for 2 hits.
    - Looks cute.
    - makes goofy noise when hit.
- Sick Beats
    - Upgrade to boombox that gives buffs to players in radius.
    - Default is movement speed and damage.
    - Configurable additional buffs are defense and stamina regen.
    - Values are completely configurable.
- Wheelbarrow & Shopping Cart
    - Two handed item that lets you carry other items.
    - Makes some noise when moving.
    - poor maneuverability.
    - Wheelbarrow is purchased in store, shopping cart is rare scrap.
- Extend Deadline
    - Extend current quota by x days.
    - EX: extend deadline 2 -> you will now have 2 more days.

### Fixes and small changes / additions
- Movement speed, jump force, stamina regen, and health is now being changed through a more considerate system. This should lead to better compatibility with other mods that also access these variables politely.
- Config option to keep upgrades after quota failure.
- Saving and loading will work in LAN now.
- More verbose logging for easier debugging.
- Upgrade sales will now save and load.
- forcecredits is host only
- store items like Peeper are now synced from hosts client as well.

## Compatibility

### This mod changes and patches a lot so problems may arise.  
- More company will break the Peeper item at the moment. Bigger lobby or advanced company's player cap solution should be more reliable.
- LC Better Saves will cause upgrades from one save file to continue to the next.
- Use common sense, EX: if you download a mod that changes the movement speed of the player every frame and the movement speed upgrade from my mod doesn't work that's why.


## Community

### Please post bugs, assets, or ideas [in this modding discord](https://discord.gg/hzEcKFSSDX) in the mod-releases forum channel [on this post.](https://discord.com/channels/1168655651455639582/1178407269994594435) 
*This mod is now mostly maintained by @whitespike. I will still merge, build, and update at his discretion.*

Feel free to [create a pull request](https://github.com/Malcolm-Q/LC-LateGameUpgrades) and help with the mod.

## Credit
- GitHub Contributors
    - Dilly_The_Dillster
    - WhiteSpike - [git](https://github.com/WhiteSpike)
    - Croquetilla
    - jarylc
- Graphics / Art / Models
    - Slipsy
    - Sad Amazon
    - Bobilka
    - Pixelated Engie - [twitter](https://twitter.com/PixelatedEngie)
- Beta Testers
    - Lann
    - Kapt
    - Rootbeer
    - Glitched
    - a glitched npc - [twitch](https://www.twitch.tv/a_glitched_npc)

## Upgrades & Items
***Everything is tweakable/removeable via the config***

- **Shutter Batteries - $300**
    - Increase the time the doors can spend closed.

- **Scrap Insurance - $400**
    - Prevents you from losing scrap on team wipe for your next moon.

- **Extend Deadline - $800**
    - Extend current quota by x days.
    - EX: extend deadline 2 -> you will now have 2 more days.

- **Wheelbarrow & Shopping Cart - $400**
    - Two handed item that lets you carry other items.
    - Makes some noise when moving.
    - poor maneuverability.
    - Wheelbarrow is purchased in store, shopping cart is rare scrap.

- **Sick Beats - $500**
    - Upgrade to boombox that gives buffs to players in radius.
    - Default is movement speed and damage.
    - Configurable additional buffs are defense and stamina regen.
    - Values are completely configurable.

* __Helmet - $750__
    - Blocks incoming damage for 2 hits.
    - Looks cute.
    - makes goofy noise when hit.

* __Diving Kit - $650__
    * Breathe underwater.
    * Heavy, two handed, low visibility.

* __Stimpack - $600__
    * Increase health by 20 per level.

* __Hunter - $700__
    * Allows you to collect and sell samples from killed monsters
    * **Lvl 1**: Hoarding Bugs & Snare Fleas
    * **Lvl 2**: Spiders & Baboon Hawks
    * **Lvl 3**: Bracken, Thumper, & Eyeless Dog

* __Medkit - $300__
    * Allows you to heal (default 20 points).
    * Limited uses (default 3)

* __Protein Powder - $500__
    * Increase damage dealt with shovels and signs.

* __Lightning Rod - $1000__
    * Redirects lightning to the ship.
    * The closer you (and your metal object) are to the ship, the more likely the ship will attract the lightning.

* __Fast Encryption - $300__
    * Upgrades the signal transmitter.
    * Must have signal transmitter purchased.
    * Instantly sends an unrestricted message to all clients chat when using transmit.

* __Interns - $1000__
    * Replaces your dead friend with a fresh intern (revives your friend).
    * Teleports to a random location in the facility.
    * $1k per use

* __Walkie GPS - $450__
    * Upgrades the walkie talkie to show your position and time.
    * Must be holding it.
    * Useful for fog or finding home.

* __Peeper - $500__
    * Looks at coil heads for you.

* __Locksmith - $640__
    * Makes noise when picking, makes a lot of noise when failing.
    * Just run into a locked door to start the minigame.
    * Strike the pins in the order they flash to unlock the door.

* __Portable Teleporter - $300__
    * An item that when used teleports you back to the ship.
    * Keeps items.
    * 90% chance to get destroyed on use.

* __Advanced Portable Teleporter - $1750__
    * Same as above.
    * 20% chance to get destroyed on use.

* __Beekeeper - $450__
    * Circuit bees do significantly less damage to you.

* __Bigger Lungs - $600__
    * Increased sprint duration.

* __Running Shoes - $650__
    * Increased movement speed.

* __Strong Legs - $300__
    * Jump higher.

* __Malware Broadcaster - $550__
    * Instead of disabling turrets and landmines; Destroy them.
    * Can enable alternate behaviours - Exploding hazards (default), destroying, or disabling for a longer period.

* __Light Footed - $350__
    * Enemies have to be closer to hear your footsteps.
    * Applies to both walking and running.

* __Night Vision - $380__
    * Press Left Alt to toggle night vision.
    * Has self regenerating batery.
    * Pick up and lmb to equip.
    * Lose on death (by default).

* __NV Headset Batteries - 300__
    * increases regen speed and decreases depletion speed of NV
    * Can also increase range and intensity of night vision light for alternate behaviour (if enabled in the config).

* __Discombobulator - $450__
    * Enter `initattack` into the terminal to stun enemies around the ship.
    * Enter `cooldown` to view cooldown (120 seconds).
    * Attracts enemies in a larger radius than loud horn.

* __Better Scanner - $650__
    * Level 1
        * Increase distance of Ship and Entrance pings drastically.
        * Increase distance of all other pings.
    * Level 2
        * Unlocks 5 new scan commands - scan player, scan enemies, scan scrap, scan hives, scan doors.
        * Type `info better scanner` for information on each.
    * Level 3
        * Allows you to scan scrap through walls.
        * Change the config if you also want to scan enemies through walls.

* __Back Muscles - $715__
    * Carryweight is drastically reduced.
    * % reduced increases each upgrade.
