# Wesnoth Server Startup Scripts (1.0.0)
Startup scripts for the Wesnoth Multi User Server - uses the "screen" command to manage session. This also restarts the wesnothd server process if it crashes.

---

These start up the Wesnothd server at boot time with a "screen" process.

1. Copy **wesnoth-server** into **/etc/init.d** - make sure it is executable
2. Run "**systemctl enable wesnoth-server**" (only needed once, will stick)
3. Run "**systemctl start wesnoth-server**" - starts wesnothd without restarting the server

When you want to view the Wesnoth console, just enter "**screen -r**" in your shell.

To disconnect from the Wesnoth console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/WesnothStartup/nostart**". To reenable it type "**rm /root/WesnothStartup/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
