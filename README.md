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
#include "extras\custom_loot\Configs\config.hpp"
#include "extras\custom_loot\Configs\cfgLoot.hpp"
```
