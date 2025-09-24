# Sourcemod-Server
Setup your own sourcemod servers.

- - - -	
# Appreciate my work, you can [PayPal Donate](https://paypal.me/Harry0215?locale.x=zh_TW) me

- - - -
### Server Install ###
* [L4D1](/L4D1): Setup ```Left 4 Dead 1``` sourcemod dedicated servers.
* [L4D2](/L4D2): Setup ```Left 4 Dead 2``` sourcemod dedicated servers.
* [CSS](/CSS): Setup ```Counter-Strike: Source``` sourcemod dedicated servers.
* [NMRIH](/NMRIH): Setup ```No More Room in Hell``` sourcemod dedicated servers.

### Dependencies ###
* **(Linux Only)**: [Source](https://linuxgsm.com/servers/l4dserver/)
	* Ubuntu < 22.04 : **Unsupported**
	* Ubuntu ≥ 22.04
		```
		sudo dpkg --add-architecture i386; sudo apt update; sudo apt install curl wget file tar bzip2 gzip unzip bsdmainutils python3 util-linux ca-certificates binutils bc jq tmux netcat lib32gcc-s1 lib32stdc++6 libsdl2-2.0-0:i386 lib32z1 gcc-multilib steamcmd
		```
	* Debian ≤ 10
		```
		sudo dpkg --add-architecture i386; sudo apt update; sudo apt install curl wget file tar bzip2 gzip unzip bsdmainutils python3 util-linux ca-certificates binutils bc jq tmux netcat lib32gcc1 lib32stdc++6 zlib1g:i386; sudo apt-get install zlib1g libzadc4 lib32z1 lib64z1
		```
	* Debian ≥ 11
		```
		sudo dpkg --add-architecture i386; sudo apt update; sudo apt install curl wget file tar bzip2 gzip unzip bsdmainutils python3 util-linux ca-certificates binutils bc jq tmux netcat lib32gcc-s1 lib32stdc++6 zlib1g:i386; sudo apt-get install zlib1g libzadc4 lib32z1 lib64z1
		```
	* CentOS
		```
		yum install epel-release curl wget tar bzip2 gzip unzip python3 binutils bc jq tmux glibc.i686 libstdc++ libstdc++.i686 zlib.i686
		```

### How to be Adm ###
1. open addons\sourcemod\configs\admins_simple.ini
2. add this line at the buttom of text, [Steamid Finder](https://steamid.xyz/)
    ```c
    "STEAM_X:X:XXXXXXXX" "99:z"
    ```
3. Save->Restart Server

# Others
* <b>[Sourcemod-Plugins](https://github.com/fbef0102/Sourcemod-Plugins)</b>: Plugins for most source engine games.
* <b>[L4D1/2-Plugins](https://github.com/fbef0102/L4D1_2-Plugins)</b>: Plugins for L4D1/2.
* <b>[Game-Private_Plugin](https://github.com/fbef0102/Game-Private_Plugin)</b>: Private Plugin List.
