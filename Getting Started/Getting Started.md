# Getting Started

This is a document containing the basics for Titanfall 2 Modding.
In this folder you may also find more detailed explanations for the things that are covered here.
If it is not located in this folder, there may be an entire folder dedicated to it ([Squirrel], for instance).
For instance, if you need more information that what the mod structure section here covers, visit [mod_structure] 

## Squirrel

Titanfall mods are written in Respawn Squirrel (rsquirrel), a modified version of [Squirrel](http://www.squirrel-lang.org/)

Squirrel files have extensions of .nut and .gnut.

## Mod Structure

Mods start as a folder in '\Titanfall2\R2Northstar\mods', being the name of the mod.
Within the main folder is 'mod.json', which contains the information about your mod as well as referencing the scripts it utilizes.
These scripts will go in '[main folder]\mod\scripts\vscripts'. 

Extra folders may be required as well. For instance, scripts for a new gamemode go in a '\gamemodes' folder within vscripts. 
(Someone please edit this to actually explain why this is.)