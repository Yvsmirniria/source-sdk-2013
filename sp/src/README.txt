This is the source code for Mobility Mod for Half-Life 2, version 2.
It is based on the Source SDK Base 2013 Singleplayer source code. This release
only contains the "game" and "public" folders, as the rest were unchanged from the
SDK base.

You may add all or part of the code to your own mod, as long as
* your mod is free
* you give credit, E.g. "This mod uses code from Mobility Mod for Half-Life 2 by Rob Cruickshank"
* you don't laugh at my ugly code

The terms of the Source SDK license also still apply. 

If you want to use this code in a commercial project, 
e.g. a licensed Source engine game or mod sold on steam, contact me. I can be bought.

To use this code you will need the Source SDK set up and compiling in Visual Studio first, then
add the parts of this code that you want.

The file MobilityModAddedFiles.txt lists all the source files that are new in Mobility Mod, and 
would need to be added to your project in Visual Studio. There are lots of changes to other files,
but those files should already be part of your VS projects. 

The file ModFolderImportantFiles.txt lists files from the ep2_mobility release package that you 
would need to add to your mod's release package. Lots of custom config settings, plus some sound effects and scripts
that the source code references.

The code for the core mobility features - double-jump, wallrunning, ledge-climbing and sliding - is
mostly located in the gamemovement class, and the base player classes. These are the relevant files to compare:

sp/src/game/client/c_baseplayer.cpp	
sp/src/game/client/c_baseplayer.h	
sp/src/game/client/c_playerlocaldata.h	
sp/src/game/client/in_main.cpp	
sp/src/game/client/in_main.h	
sp/src/game/server/ai_basenpc.cpp	
sp/src/game/server/filters.cpp	
sp/src/game/server/hl2/hl2_player.cpp	
sp/src/game/server/hl2/hl2_player.h	
sp/src/game/server/player.cpp	
sp/src/game/server/player.h	
sp/src/game/server/playerlocaldata.h	
sp/src/game/shared/baseplayer_shared.cpp	
sp/src/game/shared/gamemovement.cpp	
sp/src/game/shared/gamemovement.h	
sp/src/game/shared/gamemovement_duck.cpp	
sp/src/game/shared/gamemovement_mobility.cpp	
sp/src/game/shared/movevars_shared.cpp	
sp/src/game/shared/movevars_shared.h	
sp/src/game/shared/player_mobility_defs.h	
sp/src/game/shared/shareddefs.h	


Airboat rockets:

sp/src/game/client/c_vehicle_airboat.h	
sp/src/game/client/hl2/c_vehicle_airboat.cpp	
sp/src/game/client/hud_abrockets.cpp	
sp/src/game/server/hl2/npc_attackchopper.cpp	
sp/src/game/server/hl2/vehicle_airboat.cpp	
sp/src/game/server/hl2/weapon_rpg.cpp	
sp/src/game/server/hl2/weapon_rpg.h	
sp/src/game/server/player.h	
sp/src/game/server/vehicle_base.h	
sp/src/game/shared/gamemovement.cpp	

My hack for a gauntlet timer is in the math_counter entity, in 
sp/src/game/logicentities.cpp

Basically if you create a math_counter in hammer and name it "mob_stopwatch", it will act as a stopwatch, 
with InputAdd starting it and InputGetValue stopping it and displaying the time and best time as a HUD hint.

Grenade button:

sp/src/game/client/hl2/hud_frag.cpp
sp/src/game/client/hl2/hud_fragcount.cpp
sp/src/game/server/hl2/grenade_frag.cpp
sp/src/game/server/hl2/weapon_frag.cpp
sp/src/game/server/player.cpp
sp/src/game/server/player.h
sp/src/game/server/weapon_frag.h
sp/src/game/shared/baseplayer_shared.cpp
sp/src/game/shared/movevars_shared.cpp

Melee button and combos:

sp/src/game/client/c_baseplayer.cpp	
sp/src/game/client/c_baseplayer.h	
sp/src/game/client/hud_hintdisplay.cpp
sp/src/game/server/baseanimating.cpp	
sp/src/game/server/baseanimating.h	
sp/src/game/server/basebludgeonweapon.cpp	
sp/src/game/server/basebludgeonweapon.h	
sp/src/game/server/hl2/npc_zombine.cpp	
sp/src/game/server/hl2/weapon_crowbar.h	
sp/src/game/server/player.cpp	
sp/src/game/server/player.h	
sp/src/game/shared/basecombatweapon_shared.cpp	
sp/src/game/shared/basecombatweapon_shared.h	
sp/src/game/shared/baseplayer_shared.cpp	
sp/src/game/shared/hl2/basehlcombatweapon_shared.cpp	
sp/src/game/shared/player_mobility_defs.h	

Speedometer:

sp/src/game/client/hud_speedo.cpp

Unlocked FOV:

sp/src/game/client/hl2/clientmode_hlnormal.cpp
sp/src/game/client/view.cpp
sp/src/game/shared/baseplayer_shared.cpp
sp/src/game/shared/gamerules.cpp

There's more, but this should get you started. 


