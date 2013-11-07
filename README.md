Credits
=================
AVendettaForYou.. @ http://opendayz.net/threads/tutorial-custom-loot-tables-and-adjusting-spawn-rates.11589


All the Epoch Devs for making the mod  @ https://github.com/vbawol/DayZ-Epoch



Instructions
============

Copy mpmission/* -> your mission file


Edit your (mission file)/init.sqf

```
call compile preprocessFileLineNumbers "fixes\init\variables.sqf";
```

edit your (mission file)/description.ext

Add at the top of the file
```
#include "extras\custom_loot\Configs\CfgBuildingLoot.hpp"
#include "extras\custom_loot\Configs\CfgLootSmall.hpp"
#include "extras\custom_loot\Configs\cfgLoot.hpp"
```

Also u will need to mission fix the following in your compiles.sqf
```
player_spawnCheck =         compile preprocessFileLineNumbers "extras\custom_loot\compile\player_spawnCheck.sqf";
building_spawnLoot =        compile preprocessFileLineNumbers "extras\custom_loot\compile\building_spawnLoot.sqf";
building_spawnZombies =        compile preprocessFileLineNumbers "extras\custom_loot\compile\building_spawnZombies.sqf";
zombie_generate =             compile preprocessFileLineNumbers "extras\custom_loot\compile\zombie_generate.sqf";            //Server compile, used for loiter behaviour
wild_spawnZombies =         compile preprocessFileLineNumbers "extras\custom_loot\compile\wild_spawnZombies.sqf";            //Server compile, used for loiter behaviour
spawn_loot =                compile preprocessFileLineNumbers "extras\custom_loot\compile\spawn_loot.sqf";
spawn_loot_small =                compile preprocessFileLineNumbers "extras\custom_loot\compile\spawn_loot_small.sqf";
```
