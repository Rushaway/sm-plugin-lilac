# Little Anti-Cheat

Little Anti-Cheat is a free and open source anti-cheat for source games, and runs on SourceMod.\
It was originally developed for some secret servers I had back in the day.\
But, as I quit cheating and quit having servers, I decided to release this project to help the community out.\
This Anti-Cheat is by no means perfect, and it is bypassable to some extent, but it should still be helpful in dealing with cheaters :)

### Current Cheat Detections:
 - Angle-Cheats (Legit Anti-Backstab (TF2), Basic Anti-Aims and Duckspeed).
 - Chat-Clear (When cheaters clear the chat).
 - Basic Invalid ConVar Detector (Checks if clients have sv_cheats turned on and such).
 - BunnyHop (Bhop).
 - Basic Projectile and Hitscan Aimbot.
 - Basic Aimlock.
 - Newlines in names.

### Misc features:
 - Angle-Cheats Patch (Patches Angle-Cheats from working).
 - Max Interp Kicker (Kicks players for attempting to exploit interp (cl_interp 0.5)).
 - Max Ping Kicker (Kicks players for having too high ping (Disabled by default)).
 - Backtrack Patch (Patches backtrack cheats (Disabled by default)).
 - Macro detection.
 - Invalid name detection.
 - Invalid characters in chat patch (+ chat clear exploit fix).

### Supported Games:
 - [TF2] Team Fortress 2
 - [CS:S] Counter-Strike:Source
 - [L4D2] Left 4 Dead 2
 - [L4D] Left 4 Dead
 - [DoD:S] Day of Defeat: Source

### Untested, but should work in:
 - [HL2:DM] Half-Life 2:DeathMatch

## FAQ
**Q: What is Autoshoot?**\
A: Autoshoot is when a cheat fires a perfect 1-tick shot.\
It's quite common for cheats to do this when using aimbot.\
Autoshoot detections work by detecting 1-tick perfect shots that lead to a kill twice in a row (Autoshoot will get logged if another aimbot type was detected tho).

You *can* get a false positive for Autoshoot, but that should be very rare.\
It is possible to trigger a false positive if you use "bind mwheeldown/up +attack", as scroll (for some reason) does perfect 1-tick input.\
That said, if someone has to go out of their way to do something stupid and abnormal to get a ban, they've basically asked for it.\
If this is a problem for you, you can set `lilac_aimbot_autoshoot` to `0`.

Important thing to note about Autoshoot, because this feature shoots for you, you cannot tell if someone is using Autoshoot by spectating them, or through STV demos. Autoshoot isn't visible in demos or for spectators.

**Q: What is NoLerp?**\
A: "NoLerp" is when cheats set their interpolation to 0ms (or lower than the minimum possible).\
This is often done to increase their Aimbot accuracy.

**Q: What are Angle-Cheats?**\
A: Angle-Cheats is when a player's view angles are set beyond the limits of the game.\
This is often done to create a desync between their model and hitbox, making it harder to shoot them.\
It can also be done to execute some other exploits; like in TF2 with Duckspeed.

Note: Lilac currently does not check for yaw, so some desyncs are still possible and not detected.

**Q: Are Macros cheats?**\
A: No.\
Macros are just when a player is using a script to input buttons for them (AutoHotKey for instance), or by using scroll to spam some input.\
This is why Macro detections can only ban for 15 to 60 minutes, and no more.\
Macro detections are by default disabled, because most servers don't care about this.

**Q: Does Lilac ban for high ping?**\
A: Not quite.\
The optional high ping kicker (which is disabled by default) in Lilac bans players for 3 minutes, after that, they can reconnect.\
The reason for this is simple, if you only kicked high ping players, they could instantly reconnect.

## Non-Steam versions / CS:S v34 / CS:S v91 / ETC...
Non-Steam versions (IE: Cracks) **ARE NOT SUPPORTED!**\
I am sorry to say, but non-steam versions aren't supported.\
This is because of technical problems with cracks, as they tend to be of older versions of the game, which means they'll have bugs that can conflict with some cheat detections.\
And I just don't want to support piracy.\
I also just don't want to download sketchy unofficial cracked versions of games...

So Little Anti-Cheat may not work out of the box for cracked versions of games.\
That said, I've decided to be a little helpful based on feedback from others.

For Non-Steam/Cracked version of CS:S (like v34 or v91), Angle-Cheat detections won't work.\
You can fix this by updating these ConVars: `lilac_angles 0` and `lilac_angles_patch 0`.\
These **HAVE** to be disabled.

### Credits / Special Thanks to:
 - J_Tanzanite... Yeah I'm crediting myself for writing this AC...
 - Azalty, for being (rightly) stubborn regarding an issue and for contributing database logging.
 - foon, for fixing sourcebans++ not working (https://forums.alliedmods.net/showthread.php?p=2689297#post2689297).
 - Bottiger, for fixing this plugin not working in CS:GO and general criticisms.
 - MAGNAT2645 for suggesting a cleaner method of handling convar changes.
 - Larry/LarryBrains for informing me of false Angle-Cheat detections in L4D2.
 - [VintagePC](https://github.com/vintagepc) for SourceIRC support and basepath fix.

### Current languages supported:
 - Simplified Chinese (by [RoyZ](https://github.com/RoyZ-CSGO) ^-^, and apples194)
 - Dutch (by snowy UwU OwO EwE).
 - Danish (by kS the Man / ksgoescoding c:).
 - Norwegian (by me, the translations could be better).
 - French (by Rasi / GreenGuyRasi).
 - Finnish (By [Veeti](https://forums.alliedmods.net/member.php?u=317665)).
 - English (by me lol duh hue hue hue).
 - Russian (by an awesome person c:).
 - Czech (by luk27official and someone else).
 - Brazilian Portuguese by [SheepyChris](https://github.com/SheepyChris), [Tiagoquix](https://github.com/Tiagoquix) and [Crashzk](https://github.com/crashzk).
 - German (by two humble nice Germans c:).
 - Spanish (by ALEJANDRO ^-^).
 - Ukrainian (by panikajo ;D).
 - Polish by [qawery](https://github.com/qawery-just-sad).
 - Turkish (by ShiroNje and R3nzTheCodeGOD).
 - Hungarian (by The Solid Lad).
 - Swedish (by Teamkiller324).
 - Latvian (by rcon420).
 - Romanian (by rigE08).


I do hope to add more languages in the future.\
But at least you can add or improve on the translations already provided.\
My friends who did some of the translations were told by me that the translations don't have to be perfect.\
Just understandable to those who don't speak English too well.

### Optional:
 - Sourcebans++
 - MaterialAdmin
 - Updater

<details>
<summary>See old Closing notes from J_Tanzanite (before SRCDSLAB fork)</summary>

I wish to thank everyone who participated in this project, it's been an interesting ride.\
As fun as it has been, I think it's time to make it official: I quit.

As some can tell, I've become fairly inactive as of late,\
as fun and interesting as this project initially was to me years ago,\
I simply don't wish to work on it anymore. Frankly, games don't interest me anymore, I've moved on.

Originally, I was planning on handing this repo over to someone else to maintain,\
and handing them some of the private detection methods I developed years ago,\
and while I did start that process, I've come to change my mind.

It would be a decision that the users of Lilac had no say in,\
and given that the surface area of attack grows the more people are brought on,\
I decided it would just be best to leave this repo as it is.\
Thus, I've decided to just archive this project.

I've done my fair share, and fixed some wrongs.\
At the end of the day, all projects come to an end at some point,\
and I think this project has served its purpose, at least as far as I've cared to carry it.

## Going forward
If you are still in dire need of an anti-cheat for TF2, look to: github.com/sapphonie/StAC-tf2

While it's not perfect (nothing is), and we have some ideological differences in how we write code - their project is good.\
On the other hand, if you still wish to use Lilac, find a fork of the project that is active by people you trust.\
Or make one yourself, it's easier than you think.

As for the private detection methods?\
I wouldn't worry about it, developers are creative and will figure it out,\
and they'll figure new patterns out too.

Thanks for everything, and farewell.
</details>
