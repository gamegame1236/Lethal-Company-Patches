# Corperate Restructure
A QoL Overhaul for Corporate Executives

---
![](https://puu.sh/JXCVg/b241ca917b.png)
![](https://puu.sh/JXFG7/2e45e2d272.png)

### Features
* Monitors **[Client]**
	* Ship Loot
	* Time of Day
	* Credits
	* Total Days (Clients will display a ? until the first day is completed)
* Navigation Monitor **[Client]**
	* Weather can be hidden from Terminal and Navigation monitor via config setting
	* Moved weather condition to top
	* Added coloring to weather condition based on hazzard
		* Disabled (Unknown) = White
		* None 				 = Green
		* DustClouds 		 = Green
		* Rainy 			 = Yellow
		* Foggy 			 = Yellow
		* Stormy 			 = Orange
		* Flooded 			 = Orange
		* Eclipsed 			 = Red

# Changelog
## 1.0.1
* Updated README.md
## 1.0.2
* Added BepInExPack to dependancies
## 1.0.3
* Upper case text to match vanilla monitors *[Suggested by nickham13]*
* Fixed credits not updating for death penalties *[Reported by Vanillaboi]*
* Added color to the weather conditions on the navigations screen
* Added ability to hide weather conditions via config for the navigation screen and terminal *[Suggested by xCore]*
* Fixed credits not updating when switching planets
## 1.0.4
* Fixed Loot not updating when players respawn
* Fixed Loot not updating after gameover *[Reported by Striker--7]*
* Added Host Eject (With Config Option)
* Refactored Patches
## 1.0.5
* Fixed Loot not updating when players grab object from ship while not in the ship room
* Fixed Loot not updating when players throw/drop object from ship while not in the ship room
* Removed checking for validated drops when updating loot, as desyncing was causing issues
## 1.0.6
* Removed Host Eject due to v47