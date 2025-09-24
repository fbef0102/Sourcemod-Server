# If you appreciate my work, you can [PayPal Donate](https://paypal.me/Harry0215?locale.x=zh_TW) me.

# Server Install
* **Step 1:** [Download NMRIH Dedicated Server](#how-to-download-nmrih-dedicated-server-files).

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
		```

* **Step 4:** Change the Launch Parameters and start server
	* (Windows) Double click ```scrds.bat``` file, this file shoud be in the same folder where scrds.exe located at
		```
		start srcds.exe -console -game "nmrih" +log on +exec server +sv_lan 0 +map "nmo_anxiety" -maxplayers 32
		```
	* (Linux) Use screen, a terminal multiplexer
		```
		./srcds_run -console -game "nmrih" +log on +exec server +sv_lan 0 +map "nmo_anxiety" -maxplayers 32
		```

# Linux Server Files/Windows Server Files
> Game: No More Room in Hell
* Main
	* **[SourceMod](https://www.sourcemod.net/downloads.php?branch=1.11-dev)**
		* **v1.11-git6970** by AlliedModders LLC

	* **[MetaMod](https://www.metamodsource.net/downloads.php/?branch=1.11-dev)**
		* **v1.11-git1156** by AlliedModders LLC

	* **[stripper](https://www.bailopan.net/stripper/snapshots/1.2/)** - Add, filter and modify map entities
		* **v1.2.2-git141** by BAILOPAN

* Extenstion
	* **[SteamWorks](https://github.com/hexa-core-eu/SteamWorks/releases)** - Exposes SteamWorks functions to Developers
		* **v1.2.4** by KyleS & hexa-core-eu

	* **[Accelerator](https://forums.alliedmods.net/showthread.php?t=277703)** - Crash Reporting That Doesn't Suck
		* **v2.5.0-cd575aa** by asherkin
		* 🟥 After 2024/5/2 update, broken in Linux system

# How to download NMRIH Dedicated Server files:
* **Step 1:** [Download SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD#Downloading_SteamCMD).

* **Step 2:** launch steamcmd , steamcmd would automatically download required files .

* **Step 3:** after it says "Loading Steam API...OK.", type
	* ```force_install_dir ./nmrih/```
	* ```login xxxx```
		* xxxx is your steam account number 
		* Enter your steam account password if needed (first time login)
	* ```app_update 317670 validate```

* **Step 4:** Finish downloading and close steamcmd.
	* ```exit```

* **Step 5 (Linux Only) Dependencies** 
	* See [here](/README.md#dependencies)

# Others
* <b>[Sourcemod-Plugins](https://github.com/fbef0102/Sourcemod-Plugins)</b>: Plugins for most source engine games. Make server more fun, and more useful plugins for adm.
* <b>[Game-Private_Plugin](https://github.com/fbef0102/Game-Private_Plugin)</b>: Private Plugin List.
