# Palworld-Server-Tool

PALWORLD SERVER PANEL - SIMPLE HOW TO
======================================

1. FIRST START
--------------
1. Extract the program folder.
2. Run the Palworld Server tool
3. In the Dashboard area, choose where you want the Palworld dedicated
   server installed.
4. Let the panel find SteamCMD automatically. If SteamCMD is missing, use the
   Install SteamCMD button.
5. Click Install Server. When installation finishes, click Validate Server.

2. BASIC SERVER SETUP
---------------------
Recommended basic settings:

Server Port: 8211
Public Port: 8211
Public Lobby: ON
Public IP: Leave blank unless you specifically need to enter it.
Custom Startup Arguments: Leave blank for normal use.
sometimes server won't show up online if you don't have one!

The panel will build the normal launch arguments for you.

If people outside your home network cannot connect, make sure Windows Firewall
allows the Palworld server and that UDP port 8211 is forwarded to the server PC
in your router.

3. SERVER SETTINGS
------------------
Use the Settings tabs to configure the server.

You can change things such as:
- Server name and description
- Player limit
- Server/admin passwords
- Difficulty and XP
- Pal capture and spawn rates
- Player and Pal damage
- Hunger and stamina
- Day/night speed
- Resource rates
- Egg incubation
- Guild size
- Maximum bases per guild
- Workers per base
- Building/decay settings

Hover over a setting for a short explanation.

After changing settings, click Save before starting/restarting the server.

4. STARTING THE SERVER
----------------------
Click Start Server.

A normal public server launch should look similar to:

PalServer.exe -port=8211 -publiclobby -publicport=8211

If the panel already controls Port/Public Port/Public Lobby, do not type those
arguments again in the custom startup-arguments field.

5. MODS / WORKSHOP
------------------
Before installing mods, CREATE A BACKUP.

Recommended workflow:
1. Stop the server.
2. Open Workshop Mods.
3. Use Mod Loader Setup -> Prepare Complete Mod Environment.
4. Let the panel set up the mod folders and required components.
5. Browse the Palworld Workshop or paste a Workshop URL/ID.
6. Subscribe/download through Steam when required.
7. Click Sync All Subscribed Palworld Mods.
8. Install/enable ONE gameplay mod at a time.
9. Use Test Selected Mod Safely.
10. Let the server stay running long enough for the panel to confirm the mod.
11. Repeat for the next mod.

Do not assume every Palworld client mod works on a dedicated server. The panel
checks Info.json and looks for server-compatible install rules.

If enabling a mod causes an immediate crash:
- Use Start in No-Mod Recovery Mode.
- Restore Last Known-Good Mods.
- Test mods one at a time.
- Check for missing dependencies.
- Use Clean Old UE4SS From Win64 if you previously installed UE4SS manually.

6. BACKUPS
----------
Manual Backups:
- Click Create Backup before major changes.
- Select a backup and use Restore Selected when needed.

Auto Backup:
- Enable automatic backups.
- Choose the interval.
- Choose how many backups to keep.
- Optionally back up only while the server is running.
- Save Auto Backup Settings.

The panel must remain open for scheduled automatic backups to run.

7. UPDATES / VALIDATION
-----------------------
Use Validate Server if:
- The server suddenly stops starting.
- Files may be damaged.
- An update did not complete correctly.
- You are troubleshooting before blaming a mod.

Update Workshop mods with Update Selected or Update All while the server is
stopped.

8. QUICK CRASH CHECK
--------------------
If the server exits immediately:
1. Start with -NoMods / No-Mod Recovery Mode.
2. If it works, the problem is in the mod setup.
3. Restore the last known-good mods.
4. Add/test one mod at a time.
5. Validate the Palworld server files if it also crashes without mods.

9. IMPORTANT
------------
Always stop the server before changing, updating, or removing mods.
Back up saves before major server or mod changes.
Do not close the panel if you depend on its automatic-backup timer.
