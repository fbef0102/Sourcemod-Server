# If you appreciate my work, you can [PayPal Donate](https://paypal.me/Harry0215?locale.x=zh_TW) me.

# Server Install
* **Step 1:** [Download L4D1 Dedicated Server](#how-to-download-l4d1-dedicated-server-files).

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

		// Max players
		sv_maxplayers 8

		// Maxplayers display
		sv_visiblemaxplayers 8
		```

	2. ```cfg/server_rates.cfg```
		```php
		// For 100 Tickrate, you'd want these settings:
		sm_cvar sv_minrate 				"100000" 	// tickrate * 1000
		sm_cvar sv_maxrate 				"100000" 	// tickrate * 1000
		sm_cvar sv_minupdaterate 		"101"	 	// tickrate +1
		sm_cvar sv_maxupdaterate 		"101"		// tickrate +1
		sm_cvar sv_mincmdrate 			"101"		// tickrate +1
		sm_cvar sv_maxcmdrate 			"101"		// tickrate +1
		sm_cvar net_splitpacket_maxrate "50000" 	// (tickrate÷2) * 1000
		sm_cvar fps_max					"0"
		```

* **Step 4:** Change the Launch Parameters and start server
	* (Windows) Double click scrds.bat
		```
		start srcds.exe -console -game left4dead -tickrate 100 +log on +map l4d_vs_airport01_greenhouse +exec server +sv_lan 0 -maxplayers 31
		```
	* (Linux) Use screen, a terminal multiplexer
		```
		./srcds_run -console -game left4dead -tickrate 100 +log on +map l4d_vs_airport01_greenhouse +exec server +sv_lan 0 -maxplayers 31
		```

# Linux Server Files/Windows Server Files
> Game: Left 4 Deade 1
* Main
	* **[SourceMod](https://www.sourcemod.net/downloads.php?branch=1.11-dev)**
		* **v1.11-git6968** by AlliedModders LLC

	* **[MetaMod](https://www.metamodsource.net/downloads.php/?branch=1.11-dev)**
		* **v1.11-git1155** by AlliedModders LLC

	* **[stripper](https://www.bailopan.net/stripper/snapshots/1.2/)** - Add, filter and modify map entities
		* **v1.2.2-git141** by BAILOPAN

	* **[l4dtoolz](https://github.com/accelerator74/l4dtoolz/releases)** - Unlock Server Slot Limit
		* **v2.0.1** by ivailosp、Accelerator74

	* **[Tickrate Enabler](https://github.com/accelerator74/Tickrate-Enabler/releases)** - Unlock Tickrate
		* **v1.5** by ProdigySim、Spirit_12、Accelerator74、Forgetest

* Extenstion
	* **[REST in Pawn](https://github.com/ErikMinekus/sm-ripext/releases)** - Provides HTTP and JSON natives for plugins
		* **v1.3.1** by ErikMinekus 

	* **[socket](https://github.com/JoinedSenses/sm-ext-socket/releases)** - Provides networking functionality for SourceMod scripts
		* **v3.0.2** by sfPlayer & JoinedSenses 

	* **[sourcescramble](https://github.com/nosoop/SMExt-SourceScramble/releases)** - Memory patches & allocate memory
		* **v0.8.1.1** by nosoop

	* **[Actions](https://github.com/Vinillia/actions.ext/releases)** - Extension provides a natives to hook action event handlers and create custom actions
		* **v3.9.2** by BHaType

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
	* **[l4d_unreservelobby](https://github.com/fbef0102/L4D1_2-Plugins/tree/master/l4d_unreservelobby)** - Removes lobby reservation when server is full, allow 9+ players to join server

# How to download L4D1 Dedicated Server files:
**Warning: Don't try to download "Left 4 Dead Dedicated Server" from steam library, it's broken!! Use steamcmd instead.**

* **Step 1:** [Download SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD#Downloading_SteamCMD).

* **Step 2:** launch steamcmd , steamcmd would automatically download required files .

* **Step 3:** after it says "Loading Steam API...OK.", type
	* ```force_install_dir ./l4d1/```
	* ```login xxxx```
		* xxxx is your steam account number 
		* Enter your steam account password if needed (first time login)
	* ```app_update 222840 validate```

* **Step 4:** Finish downloading and close steamcmd.
	* ```exit```

* **Step 5 (Linux Only) Dependencies** 
	* See [here](/README.md#dependencies)

# Others
* <b>[How to install 8+ slots coop/versus server](https://github.com/fbef0102/Game-Private_Plugin/tree/main/Tutorial_%E6%95%99%E5%AD%B8%E5%8D%80/English/Game/L4D2/8+_Survivors_In_Coop)</b>
* <b>[Rotoblin-AZMod](https://github.com/fbef0102/Rotoblin-AZMod)</b>: A Competitive L4D1 Versus Configuration
* <b>[L4D1_2-Plugins](https://github.com/fbef0102/L4D1_2-Plugins)</b>: L4D1/2 enhancement, bug/glitch fixes, freaky-fun, and useful plugins.
* <b>[Sourcemod-Plugins](https://github.com/fbef0102/Sourcemod-Plugins)</b>: Plugins for most source engine games. Make server more fun, and more useful plugins for adm.
* <b>[Game-Private_Plugin](https://github.com/fbef0102/Game-Private_Plugin)</b>: Private Plugin List.
* <b>[Sourcemod Anti-Cheat-SMAC](https://github.com/fbef0102/SMAC)</b>: Server-side plugin comprised of different modules to help protect your gameserver against cheaters.
* <b>[Little-Anti-Cheat](https://github.com/fbef0102/Little-Anti-Cheat)</b>: Open source anti-cheat for source games, and runs on SourceMod.
