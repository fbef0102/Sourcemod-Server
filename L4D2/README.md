# If you appreciate my work, you can [PayPal Donate](https://paypal.me/Harry0215?locale.x=zh_TW) me.

# Server Install
* **Step 1:** [Download L4D2 Dedicated Server](#how-to-download-l4d2-dedicated-server-files).

* **Step 2:** 
	* (Windows) Choose "Windows Server files", and place the files provided in the correct folder.
	* (Linux) Choose "Linux Server files", and place the files provided in the correct folder.

* **Step 3:** Adjust cvar to match your server  
	1. ```cfg/server.cfg```
		```php
		// Set your server region to steam master
		// https://developer.valvesoftware.com/wiki/Sv_region
		// 4=Asia
		sv_region 4 

		// Max. clients/players, how many real players + bots allowed in server
		// Do not modify value (max: 31)
		sv_setmax 31

		// How many real players can join server (Not including AI Bots)
		// Free to modify value (1~31)
		sv_maxplayers 8

		// Maxplayers display
		sv_visiblemaxplayers 8
		```

	2. ```cfg/server_rates.cfg```
		```php
		// For 100 Tickrate, set these settings:
		sm_cvar sv_minrate 				"100000" 	// tickrate * 1000
		sm_cvar sv_maxrate 				"100000" 	// tickrate * 1000
		sm_cvar sv_minupdaterate 		"101"	 	// tickrate +1
		sm_cvar sv_maxupdaterate 		"101"		// tickrate +1
		sm_cvar sv_mincmdrate 			"101"		// tickrate +1
		sm_cvar sv_maxcmdrate 			"101"		// tickrate +1
		sm_cvar net_splitpacket_maxrate "50000" 	// (tickrate÷2) * 1000
		sm_cvar fps_max					"0"
		```

	3. ```cfg/l4d2_resolve_collision.cfg```
		```php
		// Multiplier of commons collision force
		// 30tick = 0.65, 60tick = 0.15, 100tick = 0.05
		z_resolve_zombie_collision_multiplier "0.05"
		```

* **Step 4:** Change the Launch Parameters and start server
	* (Windows) Double click ```scrds.bat``` file, this file shoud be in the same folder where ```scrds.exe``` located at
		```
		start srcds.exe -console -game left4dead2 -port 27016 +log on +map c2m1_highway +exec server +sv_lan 0 -tickrate 100 +sv_setmax 31
		```
	* (Linux) Use screen, a terminal multiplexer
		```
		./srcds_run -console -game left4dead2 -port 27016 +log on +map c2m1_highway +exec server +sv_lan 0 -tickrate 100 +sv_setmax 31
		```

# Linux Server Files/Windows Server Files
> Game: Left 4 Deade 2

* Main
	* **[SourceMod](https://www.sourcemod.net/downloads.php?branch=1.11-dev)**
		* **v1.11-git6968** by AlliedModders LLC	
	
	* **[MetaMod](https://www.metamodsource.net/downloads.php/?branch=1.11-dev)**
		* **v1.11-git1155** by AlliedModders LLC
	
	* **[stripper](https://www.bailopan.net/stripper/snapshots/1.2/)** - Add, filter and modify map entities
		* **v1.2.2-git141** by BAILOPAN - Modify Map
	
	* **[l4dtoolz](https://github.com/lakwsh/l4dtoolz)** - Unlock Server Slot Limit + Unlock Server Tickrate
		* **v2.4.1** by ivailosp、Accelerator74、ivailosp
	
	* **[pounce_damage_uncap](https://github.com/accelerator74/Pounce-Damage-Uncap/actions)** - Unlock Hunter Pounce Damage
		* **v1.1.0.0** by Spirit_12 & Accelerator74

* Extenstion
	* **[sourcescramble](https://github.com/nosoop/SMExt-SourceScramble/releases)** - Memory patches & allocate memory
		* **v0.8.1.1** by nosoop
	
	* **[REST in Pawn](https://github.com/ErikMinekus/sm-ripext/releases)** - Provides HTTP and JSON natives for plugins
		* **v1.3.2** by ErikMinekus
	
	* **[SteamWorks](https://github.com/hexa-core-eu/SteamWorks/releases)** - Exposes SteamWorks functions to Developers
		* **v1.2.4** by KyleS & hexa-core-eu
	
	* **[Actions](https://github.com/Vinillia/actions.ext/releases)** - Extension provides a natives to hook action event handlers and create custom actions
		* **v3.9.2** by BHaType

	* **[Resolve Collision](https://forums.alliedmods.net/showthread.php?t=344019)** - Fixes longstanding issues with low nb_update_frequency
		* **1.10.1** by BHaType

	* **[CollisionHooks](https://github.com/L4D-Community/Collisionhook)** - Provides a straightforward and easy way to hook and modify collision rules between entities.
		* **v1.3** by [VoiDeD](https://github.com/voided/CollisionHook)、[Spirit_12](https://github.com/Satanic-Spirit/Collisionhook)、A1mDev

	* **[builtinvotes](https://github.com/L4D-Community/builtinvotes/actions)** - Let plugins use the L4D/L4D2/TF2 built-in vote screens.
		* **v0.7.0** by Powerlord, A1mDev

	* **[cutlrbtreefix](https://github.com/fdxx/cutlrbtreefix/releases)** - Fixed server crash "CUtlRBTree overflow"
		* **v0.3.1** by fdxx

	* **[Accelerator](https://github.com/asherkin/accelerator/actions)** - Crash Reporting That Doesn't Suck
		* **2.6.0-manual**
		* 🟥 After SM 1.12, broken in Linux system

* Extra File
	* **[GeoLite2-City](https://www.maxmind.com/en/home)** - addons\sourcemod\configs\geoip\GeoLite2-City.mmdb
		* **2024-12-06** by MAXMIND

	* **[GeoLite2-Country](https://www.maxmind.com/en/home)** - addons\sourcemod\configs\geoip\GeoLite2-Country.mmdb
		* **2024-12-06** by MAXMIND

# Recommended Files
* Plugins
	* **[l4d2_vomit_fix](https://github.com/lakwsh/l4d2_vomit_fix)** - Patches Boomer Vomit behavior to fix an issue where vomit range scaled inversely with tickrate.

	* **[l4d2_a2s_fix](https://github.com/lakwsh/l4d2_vomit_fix)** - Patches A2S_INFO issue (Only when sv_steam_bypass is 1)

	* **[l4d_unreservelobby](https://github.com/fbef0102/L4D1_2-Plugins/tree/master/l4d_unreservelobby)** - Removes lobby reservation when server is full, allow 9+ players to join server

# How to download L4D2 Dedicated Server files:
* **Step 1:** [Download steamcmd](https://developer.valvesoftware.com/wiki/SteamCMD#Downloading_SteamCMD).

* **Step 2:** Launch steamcmd, steamcmd would automatically download required files .

* **Step 3:** After it says "Loading Steam API...OK.", type
	* ```force_install_dir ./l4d2/```
	* ```login xxxx```
		* xxxx is your steam account number 
		* Enter your steam account password if needed (first time login)
	* ```app_update 222860 validate```

* **Step 4:** Finish downloading and close steamcmd.
	* ```exit```

* **Step 5 (Linux Only) Dependencies** 
	* See [here](/README.md#dependencies)

# Others
* <b>[How to install 8+ slots coop/versus server](https://github.com/fbef0102/Game-Private_Plugin/tree/main/Tutorial_%E6%95%99%E5%AD%B8%E5%8D%80/English/Game/L4D2/8+_Survivors_In_Coop)</b>
* <b>[L4D1_2-Plugins](https://github.com/fbef0102/L4D1_2-Plugins)</b>: L4D1/2 enhancement, bug/glitch fixes, freaky-fun, and useful plugins.
* <b>[Sourcemod-Plugins](https://github.com/fbef0102/Sourcemod-Plugins)</b>: Plugins for most source engine games. Make server more fun, and more useful plugins for adm.
* <b>[Game-Private_Plugin](https://github.com/fbef0102/Game-Private_Plugin)</b>: Private Plugin List.
* <b>[Sourcemod Anti-Cheat-SMAC](https://github.com/fbef0102/SMAC)</b>: Server-side plugin comprised of different modules to help protect your gameserver against cheaters
* <b>[Little-Anti-Cheat](https://github.com/fbef0102/Little-Anti-Cheat)</b>: Open source anti-cheat for source games, and runs on SourceMod.
