# Polly's Enhanced HL2 Preset
A configuration file for Half-Life 2 that enhances the game while retaining the original style. Eventually, a full guide on Steam will also include various other tweaks, including suggested mods, all with retaining the goal of lightly enhancing the original experience. There are no major overhauls and no over the top shaders, just a minimal layer of extra polish on top of the wonderful 20th Anniversary Update.

Better documentation is forthcoming, but currently, this preset also makes a few small gameplay tweaks.

- The delay between a weapon being automatically reloaded after holstering has been dramatically increased to 90 seconds. In practice, this means that reloading actually matters in combat now, increasing tension and difficulty in a way that's manageable by the player, instead of just increasing enemy damage or health. This also means that weapons will still comfortably reload in your pocket while exploring, so you won't be caught with your pants down from a previous fight.
- The damage of Shotgun Soldiers has been reduced slightly, which should hopefully prevent them from chunking you on Hard out of nowhere. Their damage is much higher than any other Combine enemy, especially because there is a quirk with how quickly they fire related to their movement.
- Crowbar damage has been increased slightly. Honestly, the crowbar just feels like lacks a little bit of heft. It takes six(!) hits to deal with a metrocop, and while metrocops aren't so scary, later in the game most enemies are too dangerous to whack with the crowbar anyway. This is just a gentle nudge in effectiveness, since if it deals too much damage we risk discouraging the player from using the gravity gun.
- Antlion guards now deal a bit more damage. Currently, antlion guards are very easy to deal with for experienced players, even on Hard. Their attacks are extremely easy to avoid, and it's trivial to pump shotgun shells into them over and over to kill them. Increasing their health is likely to just make the fight more tedious, so instead their damage has been given a bit of a boost, which should punish players for getting complacent while still allowing them to feel powerful if they keep their guard up.

If you wish to disable these tweaks, just don't use the `pehp-balance` module.

## INSTALLATION
For now, you'll just have to download the file from Github manually. Make sure the file is placed in: `steamapps\common\Half-Life 2\hl2_complete\cfg`

There will hopefully be a more elegant way to do this in the future, but for now, you should also download these addons:
<https://gamebanana.com/mods/35608>

## TWEAKING
You can manually set up a `preferences.cfg` file in the same directory as the main `autoexec.cfg` file. Any commands in this file will override the ones in `autoexec.cfg`. For example, you can use this to set your `default_fov` to `90`.

## UPDATING
Just override `autoexec.cfg` while retaining your `preferences.cfg`.

## MISC
Right now, the config also includes a keybind called `togglehud`, which will toggle both the HUD as well as your weapon viewmodel for taking clean screenshots. This is bound to `.` by default. You can also type `enhance` in the console to run the preset again, assuming it loaded correctly the first time. `[` will re-enable achievements by disabling commentary mode and cheats, then quicksaving and immediately reloading. This will enable cheats again.

### Fun and Useful Commands
- **snd_restart** - Restart the game's sound system. This command is preferred over stopsound as it will actually restart things like soundscapes.
- **toggle_duck** - Toggles crouch, as opposed to `+crouch` which is a hold.
- **ai_force_serverside_ragdoll 0** - Toggles serverside ragdolls. This has many interesting effects, the most notable of which is that ragdolls can be interacted with by physics props, entities, and NPCs (but not by the player or other ragdolls). This can often cause undesired behavior, such as enemies suddenly snapping into the air when walking over bodies, so it's not included in the main file.
- **ent_fire** - can be used in a ton of ways. Either pick an entity whose name you know or use !picker for what you're looking at (this can target invisible entities as well, so it may behave unexpectedly without extra visualization commands). Funny subcommands include delete and ignite.
- **print_froggy**, **print_sparkles**, **print_sparklyfroggy** - Well? Just try it out for yourself!

### Useful Cvars
- **r_flashlightlockposition 1** - *Cheat.* "Lock the flashlight to whatever position it was created at, making it independent of the player. Will delete itself when turned off." - V92 Default: 0
- **sv_stickysprint 1** - Toggles whether or not sprint is toggled instead of held. Default: 0
- **snd_mute_losefocus 1** - Toggles whether or not audio will be muted when focus is lost. Default: 0
- **mat_tonemap_algorithm 0** - Restores tonemap to retail Episode One stylized tonemapping. Supposedly, this was changed with the release of Episode Two in order to avoid a bug with the Jalopy's lights. Default: 1
- **mat_hdr_uncapexposure 1** - Uncaps exposure to match retail Episode One. Default: 0
- **r_radiosity 4** - Level of radiosity. 4 is the only value not listed in the console description - cool. 2 supposedly looks better, but can rarely cause issues with props that have vertices clipping into map geometry. Default: 4

### Broken Cvars
- **g_ragdoll_maxcount 256** // Amount of ragdolls that will exist in a map at once. As of Dec 2024, this value does not seem to do anything. Source will become unstable if there are too many ragdolls even on modern hardware, so this is clamped to a relatively sane value. There are few maps in Vanilla HL2 that can even generate this many ragdolls, but this should prevent instability on custom maps. Default: 8
- **g_ragdoll_important_maxcount 10** // Amount of larger ragdolls that will exist in a map at once, such as Striders. There aren't any vanilla maps that should go over even the default value, so this is largely for community maps. Notably, it seems like an "important" ragdoll is probably something set in Hammer, as this value does not affect larger enemies spawned in testing. I have no idea if this value actually does anything in practice. Default: 2
- **cl_ragdoll_collide 1** // Toggle whether generated ragdolls collide with each other. Seems to have been broken since Orange Box according to the developer wiki, and currently doesn't function as of Nov 2024. Seems like it can also occasionally cause issues. Default: 0

## CONTACT
If you would like to report bugs, make suggestions, or have any other feedback, please feel free to open an issue on GitHub for the time being.

## CHANGELOG
#### 0.0.2 - 01 December 2024
- Added some some gameplay tweaks using a looping .cfg script for now.

#### 0.0.1 - 25 November 2024
- Initial version.