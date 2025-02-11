Protector Plugin
================================
 
### About

This plugin provides players on TShock driven Terraria servers the possibility of taking ownership of certain objects or blocks, so that other players can not change or use them.
The content of a protected chest can not be viewed or altered by other players, protected switches can not be hit by other players, signs can not be edited, beds can not be used, doors not opened and even plants in protected clay pots can not be harvested without owning the clay pot.

And if a player wants to access items of a friend's chest, then the owner of it shall share it with them. Protector offers sharing of protections directly to specific users, to TShock user groups or just to everyone - and it's the owner of the protection doing that, no administrative actions required.

Stay in control, you define which blocks or objects can be protected, are automatically protected on placement, can be deprotected, how many protections a player can create in general and what can be shared or not.

Furthermore, one might make use of Protector's special chest related features, like powerful Refill Chests allowing a timed refill of their content, restrict players from looting them more than one time or allowing only X times of lootings in total. 
Also, if your server happens to change worlds frequently or if you just want to offer your players to use chests which can be easily transported including their content, then you can allow the usage of so called Bank Chests storing their content world independently - imagine them as server sided piggy banks.

Usually Terraria worlds are limited to a maximum of 1000 chests. By using Protector you may bypass this limitation, check out the comments in the configuration file to see how this is done.

Releases of this plugin use [Semantic Versioning](http://semver.org/).

### How to Install

Note: This plugin requires [TerrariaAPI-Server](https://github.com/NyxStudios/TerrariaAPI-Server) and [TShock](https://github.com/NyxStudios/TShock) in order to work. You can't use this with a vanilla Terraria server.

Grab the latest release and put the _.dll_ files into your server's _ServerPlugins_ directory. Also put the contents of the _tshock/_ folder into your server's _tshock_ folder. You may change the configuration options to your needs by editing the _tshock/Protector/Config.xml_ file.

### Commands

* `/protect [-p]`
* `/deprotect [-p]`
* `/protectioninfo [-p]`
* `/share <player name> [-p]`
* `/unshare <player name> [-p]`
* `/sharegroup <group name> [-p]`
* `/unsharegroup <group name> [-p]`
* `/sharepublic [-p]`
* `/unsharepublic [-p]`
* `/bankchest <number>`
* `/dumpbankchest`
* `/refillchest [time] [+ot|-ot] [+ll amount|-ll] [+al|-al] [-p]`
* `/refillchestmany <selector> [time] [+ot|-ot] [+ll amount|-ll] [+al|-al] [-p]`
* `/lockchest [-p]`
* `/swapchest [-p]`
* `/tradechest <sell amount> <sell item> <pay amount> <pay item or group> [limit]`
* `/protector`
* `/protector commands`
* `/protector removeemptychests`
* `/protector summary`
* `/protector cleanup [-d]`
* `/protector removeall <region <region>|user <user>> [-d]`
* `/protector importinfinitechests`
* `/protector importinfinitesigns`
* `/protector reloadconfig|reloadcfg`

To get more information about a command type `/<command> help` ingame.

### Permissions

* **prot.manualprotect**
  Can manually create protections (not required for auto protection).
* **prot.manualdeprotect**
  Can manually remove owned protections (not required for auto deprotection).
* **prot.chestshare**
  Can share Chests.
* **prot.switchshare**
  Can share Switches / Levers / Pressure Plates / Timers / Music Boxes.
* **prot.othershare**
  Can share Signs, Tombstones and Beds.
* **prot.sharewithgroups**
  Can share protections with TShock Groups.
* **prot.setbankchest**
  Can set up bank chests.
* **prot.bankchestshare**
  Can share bank chests.
* **prot.nobankchestlimits**
  Can set up unlimited bank chests.
* **prot.dumpbankchest**
  Can dump bank chest content (Warning: duplicates the bank chest's items).
* **prot.nolimits**
  Can create an unlimited amount of protections.
* **prot.viewall**
  Can view all information of all protections. Usually only owners or shared
  players can view extended information of a protection.
* **prot.useeverything**
  Can use and any Chest, Sign, Switch, Lever, Pressure Plate etc. (does 
  not include removing them though).
* **prot.protectionmaster**
  Can modify or remove any protection, can also alter any refill chest if 
  "prot_setrefillchest" is also given.
* **prot.setrefillchest**
  Can set up a chest to automatically refill its content.
* **prot.settradechest**
  Can set up a trade chest to trade items with other players.
* **prot.freetradechests**
  Doesn't have to pay SEconomy money to set up a trade chest.
* **prot.utility**
  Can display a summary about all chests, signs and protections of a world, can 
  lock chests, can convert all dungeon chests, sky island chests, ocean chests, 
  hell shadow chests to refill chests (also requires "prot_setrefillchest"), can 
  remove all empty non protected chests of the world, can swap chest data storage.
* **prot.cfg**
  Can import Infinite Chests' data or Infinite Signs' database files, can 
  reload Protector's configuration file.
* **prot.regionsonlyprotections**
  Can only create protections in regions with build permissions.

### Data Import and Compatibility

This plugin can import chest and sign data from the Infinite Chests and Infinite
Signs plugins. Make SURE you create world backups before using this functionality
as those changes can otherwise not be revoked. 
Note that the import features aren't very well tested, especially not with more
recent versions of the plugins.

It's also limited to regular- and refill chests. Bank chests will not be imported. 
Also, region chest protection and chest passwords are not supported by Protector.
If your infinite chests database holds more than 999 chests, all exceeding chests
**should** become protector chests.

Do NOT try to use any chest features of Protector together with Infinite Chests 
as this will cause mixed item data in the world file and the chest database.

### Credits

Icon made by [freepik](http://www.freepik.com/)
