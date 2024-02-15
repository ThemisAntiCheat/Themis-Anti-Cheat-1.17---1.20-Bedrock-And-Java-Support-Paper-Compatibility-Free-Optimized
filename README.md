# Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized
A free Anti Cheat focused on Accuracy, Efficiency and Simplicity

This plugin only works on Minecraft versions 1.17.X, 1.18.X, 1.19.X and 1.20.X!

You need to install ProtocolLib to use Themis! It is highly recommended to use version 5.0 or later (at the time of writing, this means a dev build) for performance reasons. Older versions will work but will have worse performance!

For Bedrock support you need to install the Bukkit/Spigot version of Floodgate (both 1.0 and 2.0 are supported)!

If you're using ViaBackwards, you need version 4.1.0 or higher for the ping measurements to work correctly.

If there are any issues, instead of leaving a bad review please join the Discord so that we can help you!
![image](https://github.com/ThemisAntiCheat/Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized/assets/160132059/22023c75-81f7-4f6b-af0c-a89f45436ada)

Themis is an anti cheat with a focus on accuracy, efficiency and simplicity.

I highly recommend joining the Discord server to stay up to date and get support.

Themis supports Spigot, Paper and Tuinity. Other forks will probably work too, but I don't guarantee it.

Also Themis has real Bedrock/Geyser support! By "real" I mean that it actually performs proper checks on Bedrock players. Some other anti cheats simply exclude Bedrock players from the checks, which means that they can fully bypass the anti cheat. With Themis this is not the case!

Note that supporting Bedrock is more difficult than Java since it's a completely different codebase and Geyser has bugs that cause random weird behaviour (Geyser is an absolutely amazing piece of software though!), so there will be false positives. Please report them on Discord to help me fix them!

Themis has a flexible config that allows you to configure an arbitrary number of actions that can consist of an arbitrary number of commands which should be run. For each action you can define a minimum score required to run, and a score and time delay for it to be run again. All of this can be configured for each check individually. You can find the config in the config section below.

Themis currently focuses on movement hacks but will expand and detect more hacks in the future.

If you want to support my work on Themis, you can donate on my Patreon page.

The plugin Anti Cheat Replay supports Themis and can be used to record players when getting punished by Themis so that the recordings can be reviewed and used as evidence later.

![image](https://github.com/ThemisAntiCheat/Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized/assets/160132059/f67bb97a-95ff-43d3-b9f3-536cb2b084e3)

BHop Speed
Blink
Boat Fly
Boat Speed
Climb / Spider
Elytra Fly
Fly
Jetpack
KillAura if it uses increased Reach
NoFall
OnGround Speed
Reach
Step
Timer
Vanilla Speed
WaterWalk / Jesus
Note that this list is not complete. Some checks can catch hacks they weren't even designed for, and some hacks can have many different names in different hack clients, so even if a hack is not on this list, there's a chance it's blocked anyways, especially if it's similar to the ones listed.

![image](https://github.com/ThemisAntiCheat/Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized/assets/160132059/4f264b07-2be7-4bf6-b1f2-cfdfa94f1e57)

Themis doesn't just promise efficiency, it also delivers it. This is a timings report over an hour of a server running Themis 0.8.1 with all checks enabled and about 15 players online.
[​IMG]
It shows that on average Themis uses 0.23% of the tick, which is about 0.015% per player. Of course this number will vary, depending on your server hardware and setup (plugins, gamemodes, ...).

For comparison, as of writing this (13th April 2021), AAC has a similar statistic on its plugin page where it uses 3.92% for 140-150 players which is about 0.026% to 0.028% per player, so Themis is almost twice as fast.

(Note that this is not at all a fair comparison since AAC has a lot more features than Themis! I didn't put this here to say Themis is better, I just think the statistic alone will be meaningless to most people, so I wanted some reference point, and I chose AAC because it's a well optimized anti cheat, it's widely known and it has a similar statistic on its plugin page.)

If you notice any mistakes in these calculations please let me know!
![image](https://github.com/ThemisAntiCheat/Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized/assets/160132059/84a078e8-a680-4326-88df-be8424fb7ec3)

![image](https://github.com/ThemisAntiCheat/Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized/assets/160132059/ecea70bb-92d3-4f8a-aff1-ec4975f88abe)

To install Themis, please carefully follow these steps:
Make sure you're running version 1.17.X, 1.18.X or 1.19.X of Spigot or Paper. Other forks will probably work too, but I don't guarantee it.
Check if ProtocolLib is already installed on your server. If not, please download it here. Note that depending on your server version, you might need a specific version, please read the ProtocolLib plugin page carefully. Even if it's already installed, I recommend redownloading it to make sure it's up to date and contains no old bugs.
Download the Themis .jar file from this page and drop it in your plugins directory.
Only if your server allows Bedrock players: Install Floodgate to allow Themis to check if a player is using Bedrock and to adjust the checks accordingly (both 1.0 and 2.0 are supported). Note that you need the Bukkit version installed on every server where Themis is running, the Bungee version is not enough! If you're using Bungee, you need to set the "send-floodgate-data" option in the Bungee Floodgate option, otherwise the Floodgate API won't work. It is also highly recommended to enable "forward-player-ping" in the Geyser config, otherwise Themis will not be able to measure the ping of Bedrock players.
Now restart the server, to make it load all the changes. Run /themis to check if the installation worked. If it didn't, please check the troubleshooting section below.
Only if your server allows Bedrock players: Run "/themis info [PlayerName]" on a Bedrock player and make sure Themis correctly reports it as a Bedrock player, otherwise something with your Floodgate setup is wrong. If not, make sure you enabled the "send-floodgate-data" like mentioned above and join the Discord server for assistance.
![image](https://github.com/ThemisAntiCheat/Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized/assets/160132059/48da64a1-1dbf-4390-ab01-9075c65f9c31)

![image](https://github.com/ThemisAntiCheat/Themis-Anti-Cheat-1.17---1.20-Bedrock-And-Java-Support-Paper-Compatibility-Free-Optimized/assets/160132059/03fa9f48-920c-416a-b611-b88ddf5d0da1)

Problem: Themis isn't working
If you installed Themis, but it didn't work, please try running /themis to see if Themis is running. Note that you need the themis.command.info permission, by default everyone has it but your permission plugin might be disabling it.
If it worked: This means that Themis was loaded and is running correctly. If you're not getting any detections, first please check the "Blocked Hacks" section below make sure that the hack your testing is supported by Themis. If it is, it might not show up because you have the bypass permission. This is disabled by default (even for ops), but you might get it from your permissions plugin, e.g. if you have * perms. If you have LuckPerms, you can use "/lp user [Username] permission check themis.bypass" to see if you have the permission, other permission plugins probably offer similar commands. If you're sure that Themis is running and that you don't have the bypass permission, but you're still not getting any detections, please join the Discord for assistance.
If it didn't work: This mean that something went wrong while loading Themis. Try running /pl and see if Themis shows up.
If it doesn't show up, it probably means that you didn't place the .jar file in the right directory, or you didn't restart the server after doing so. Make sure the .jar file is in the plugins directory and restart the server. If this doesn't help, please join the Discord for more information.
If it shows up in red, this most likely means that you're either not on a supported Minecraft version or you didn't install ProtocolLib. If neither of these is the problem, please check the logs for more information and join the Discord for assistance.​
When asking for support on Discord because something is not working, please directly include the log file. It contains a lot of helpful information and will make helping you easier and faster!

Problem: Bedrock players are getting flagged
Run /themis info [player name]" on a Bedrock player and check if Themis correctly detects them as a Bedrock player. If not that means you don't have Floodgate set up correctly. This is not a Themis issue! Often this can be solved by changing the "send-floodgate-data" in the Bungee/Velocity Floodgate config to true.

Problem: Bedrock players always have 0 ping
You need to enable the "forward-player-ping" option in the Geyser config.
