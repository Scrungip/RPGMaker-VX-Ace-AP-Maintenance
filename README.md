# Maintenance Fork for RPGMaker VX Ace AP
 This fork has a few quality of life changes for usage with current AP versions as well as fixing a couple standing issues with the existing implementation.
 1. The script now has an option that can limit item receiving to the standard map scene, which can help with issues that may stem from things happening during battle or other scenes.
 2. The Datapackage Cache system has been rewired a bit to support game titles that contain symbols not supported in file/folder names.
 3. I've included Hime's Common Event Queue script, as it fixes some issues with Common Events that become very apparent when using them as AP Items. By default, reserving common events is a bit of a wild west and won't neccessarily do them in order, and if the same event is called multiple times it will only run once. This script puts it in a proper queue and runs everything as it's queued. Very handy.
 
 This is the version of the script I use for my personal projects, and I haven't had issues with it.
 Do let me know (either on here or through Discord) if you notice any issues.

Anyway, here's the original README:

# RPGMaker VX Ace AP
 Scripts that allow RPGMaker VX Ace, using mkxp-z, to connect to the Archipelago Multiworld Randomizer
		
 *Note: This readme is in a todo state but WILL be improved later*

 ## Usage
 1. Replace your RPGMaker game's executable with [mkxp-z](https://github.com/mkxp-z/mkxp-z), either by building it yourself or using an automatic build.
 2. Copy and paste the "Ruby" and "Custom" folders into the game directory. Copy and paste "mkxp.json" into the game directory and optionally configure it based on your needs.
 3. Add the contents of Archipelago_RGSS3 to your game's Scripts. (Script Editor -> Insert new script -> Paste Archipelago_RGSS3's contents into that new script)
 4. Configure the script under the CONFIGURATION section within it.
	
Your game will now be able to receive ReceiveItem packets from Archipelago!

## Notes
`$archipelago` is your client. All Archipelago-related methods must use it.
	
Call `$archipelago.get_connect` to connect to the multiworld
	
All other methods/accessors are almost identical to the ones provided by [archipelago.js](https://thephar.github.io/Archipelago.JS/)
	
Feel free to message me (Discord: eggslashether) or email me (archipelago_rb@eggslashether.com) if you have any issues! I'm always willing to help.
