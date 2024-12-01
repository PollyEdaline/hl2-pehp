Polly's Enhanced HL2 Preset
=========
A configuration file for Half-Life 2 that enhances the game while retaining the original style. Eventually, a full guide on Steam will also include various other tweaks, including suggested mods, all with retaining the goal of lightly enhancing the original experience. There are no major overhauls and no over the top shaders, just a minimal layer of extra polish on top of the wonderful 20th Anniversary Update.

Presently, this config makes two small gameplay tweaks. First, the delay between a weapon being automatically reloaded after holstering has been dramatically increased to 90 seconds. In practice, this means that reloading actually matters in combat now, increasing tension and difficulty in a way that's manageable by the player, instead of just increasing enemy damage or health. This also means that weapons will still comfortably reload in your pocket while exploring, so you won't be caught with your pants down from a previous fight.

Secondly, the damage of Shotgun Soldiers has been reduced slightly, which should hopefully prevent them from chunking you on Hard out of nowhere. Their damage is much higher than any other Combine enemy, especially because there is a quirk with how quickly they fire related to their movement.

Eventually, these may go in their own separate module. For now, you can disable these in your `preferences.cfg`.

INSTALLATION
------------
For now, you'll just have to download the file from Github manually. Make sure the file is placed in: `steamapps\common\Half-Life 2\hl2_complete\cfg`

TWEAKING
------
You can manually set up a `preferences.cfg` file in the same directory as the main `autoexec.cfg` file. Any commands in this file will override the ones in `autoexec.cfg`. For example, you can use this to set your `default_fov` to `90`.

UPDATING
------
Just override `autoexec.cfg` while retaining your `preferences.cfg`.

MISC
------
Right now, the config also includes a keybind called `togglehud`, which will toggle both the HUD as well as your weapon viewmodel for taking clean screenshots. This is bound to `.` by default. You can also type `enhance` in the console to run the preset again, assuming it loaded correctly the first time. `[` will re-enable achievements by disabling commentary mode and cheats, then quicksaving and immediately reloading. This will enable cheats again.

Some Commands
---
- **snd_restart** - "Restart the sound system of the game. It is greatly advised to use this command over stopsound as this command won't break soundscapes, soundscripts, or entity sounds" - V92
- **toggle_duck** - Toggles crouch, as opposed to `+crouch` which is a hold.
- **ai_force_serverside_ragdoll 0** - Toggles serverside ragdolls. This has many interesting effects, the most notable of which is that ragdolls can be interacted with by physics props, entities, and NPCs (but not by the player or other ragdolls). This can often cause undesired behavior, such as enemies suddenly snapping into the air when walking over bodies, so it's not included in the main file.
- **ent_fire** - can be used in a ton of ways. Either pick an entity whose name you know or use !picker for what you're looking at (this can target invisible entities as well, so it may behave unexpectedly without extra visualization commands). Funny subcommands include delete and ignite.

Useful Cvars
---
- **r_flashlightlockposition 0** - Cheat. "Lock the flashlight to whatever position it was created at, making it independent of the player. Will delete itself when turned off." - V92 Default: 0
- **sv_stickysprint 0** - Toggles whether or not sprint is toggled instead of held. Default: 0

CONTACT
-------
If you would like to report bugs, make suggestions, or have any other feedback, please feel free to open an issue on GitHub for the time being.

CHANGELOG
---------
__**0.0.1** - 25 November 2024__

Initial version.