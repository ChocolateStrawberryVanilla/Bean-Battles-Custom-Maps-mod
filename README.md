# Bean-Battles-Custom-Maps-mod
A fork of the "Custom map making/loading mod" for Bean Battles. This is a modded version of Flarfo's BeanBattlesMapMaker. Therefore, either Flarfo's version or this version should be in the Bepinx plugins folder. Not both.

Flarfo's installation guide: https://www.youtube.com/watch?v=LKqCqfUcV_A&list=PL8_A1XBIbdkKR9wXkWJudVez3ZD7q7WBU

This mod makes the map window minimizable and changes the way it scrolls. It can also hide the name of the custom map you're playing on.

# FAQ
__Why would you tag custom lobbies after going through the trouble to hide the map names?__
* I want to hide map names so that they can be as ugly as they need to be. If there is a custom map named "10478823985454" then I don't want that in my lobby title.

    I had considered adding a "pretty" map text file that gets used instead, but I felt like that might confuse non-modded players into thinking a custom map is an official BeanBattles map.

__How will I know what map I'm missing?__
* When you get booted to the main menu an error message will appear in the top left, telling you which map you're missing.

__How do I keep the map window changes, but the old lobby naming system?__
* Use release version 2.13 or recompile using the patch that allows map names in lobby titles.
    * Doing this should also make this mod compatible with lobbies using Flarfo's original map mod.

# Changelog
### Feb 26, 2025
* Made scrolling non-elastic
* Modified map window to make it collapsable
* Added a minimize window button
* Changed instances of `transform.parent=` to `transform.SetParent(...)` to mitigate console warning spam

### July 18, 2025
* Updated to .NET 4.6
* Updated the network code to match the current Bean Battles Custom Map build
* Closing the window no longer moves the title bar
* The minimize button now changes direction based on the window being closed or open
* Cleaned up code implementation of minimizing the window
* Removed vestigal assemblies
* Fixed circular references

### July 19, 2025
* ~~Made lobby names normal by default (no more tacking on the custom map name to the lobby name)~~
    * Kept a "custom map name in lobby name" file patch that can replace the "Patches.cs" to bring back the old system when compiling the dll
    * Added the name of the map you're missing to the "missing map" error message to compensate for the lobby name changes

### October 13, 2025
* Hidden map names in lobby titles have been re-implemented with the Halloween update (thanks Duck!)
* Custom lobbies now have a "Custom Map" tag added to the lobby name to help differentiate them from normal lobbies
    * Map names will not affect this tag
* Changed the patch that searches a lobby's name for the custom map to "Patches-Lobby-Name.cs" for clarity
