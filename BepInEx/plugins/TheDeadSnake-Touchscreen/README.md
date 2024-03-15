# Touchscreen
Upgrade your ship monitor with a touchscreen.
![](https://raw.githubusercontent.com/TheDeadSnake/LC-Touchscreen/master/images/MonitorHover.png)

Once you load into a level you can hover over the monitor and click away.
* <b>Interact</b> <i>(def. E)</i>:<br>
 \> Switch view to a player<br>
 \> Trigger Doors, Land mines or Turrets<br>
 \> Ping a radar

* <b>Use</b> <i>(def. LMB)</i>:<br>
 \> Use the Flash feature of a radar booster<br>

* (Optional) <b>QuickSwitch</b> <i>(def. Unused)</i>:<br>
 \> Switch between radar targets (Does the same as the button on the monitor)<br>
 
* (Optional) <b>Alt QuickSwitch</b> <i>(def. Unused)</i>:<br>
 \> Reverse radar target order (Exact behaviour depends on config setting)<br><br>

# Changelog:
### Version 1.1.0:
* Fix compatibility with LethalLevelLoader
* Added support for InputUtils
### Version 1.0.10:
* Fix compatibility with GeneralImprovements
* Fix issue if UseOriginalLethalExpansion of LethalExpansionCore is used (Due to 1.0.9)
### Version 1.0.9:
* Added option to enable / disable the pointer (cursor) when hovering over the monitor
* Fix compatibility with LethalExpansionCore on custom moons
### Version 1.0.8:
* Fix support for custom moons<br>
 \> Updated .NET Framework to v4.7.1
* Fixed NPE error (Old Reference) after v1.0.7 update
### Version 1.0.7:
* Added additional optional key bind
* Added config option to decide behaviour of the new optional key bind<br>
 \> True: When key bind is pressed, the quick switch will go in the reverse order<br>
 \> False: When key bind is pressed, the previous radar target will be selected
* Radar boosters held by players will now get priority over switch camera key bind
### Version 1.0.6:
* Added optional key bind to switch monitor targets (def. unset)
* Added option to enable / disable keybind tooltips when hovering over the monitor
### Version 1.0.5:
* Fixed NPE error (Old Reference) after leaving a lobby and joining another one [Affects all versions 1.0.5>]
### Version 1.0.4:
* Added support for 3rd party plugins to disable/enable the plugin features
* Added two new monitor pointer images (Cross, Dot)
* Added two new config values:
	* Option to change out the monitor pointer image
	* Option to override if 3rd party plugins can disable/enable features (def. Allow 3rd party plugins)
* Touchscreen now only works on planets
### Version 1.0.3:
* Added config to modify key bindings
### Version 1.0.2:
* Fixed button names when using a Controller
### Version 1.0.1:
* Fixed incorrect resource path of the monitor pointer image
### Version 1.0.0
* Initial release
