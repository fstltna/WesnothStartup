# Wesnoth Server Startup Scripts (1.1.0)
Startup scripts for the Wesnoth Multi User Server - uses the "screen" command to manage session. This also restarts the wesnothd server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/WesnothStartup) - [Official Forum](https://wesnoth.gameplayer.club/index.php/forum/wesnoth-server-tools)  - [Official Download Area](https://wesnoth.gameplayer.club/index.php/downloads/category/5-wesnoth-server-tools)
![Wesnoth Sample Screen](https://wesnoth.gameplayer.club/The_Battle_for_Wesnoth.jpg)

---

These start up the Wesnothd server at boot time with a "screen" process.

1. Copy **wesnoth-server** into **/home/wesnothowner/bin** - make sure it is executable
2. Copy **runwesnoth-server** into **/home/wesnothowner/wesnoth** - make sure it is executable
3. Copy **startwesnoth-server** into **/home/wesnothowner/wesnoth** - make sure it is executable
4. Put **@reboot /home/wesnothowner/bin/wesnoth-server start** into your crontab


When you want to view the Wesnoth console, just enter "**screen -r**" in your shell.

To disconnect from the Wesnoth console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /home/wesnothowner/wesnoth/nostart**". To reenable it type "**rm /home/wesnothowner/wesnoth/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
