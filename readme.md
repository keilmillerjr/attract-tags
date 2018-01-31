# attract tags for AttractMode front end

by Keil Miller Jr [Keil Miller Jr](http://keilmillerjr.com)

## DESCRIPTION:

*attract tags* is tag files for the [AttractMode](http://attractmode.org) front end. It was designed because I was seeking an easy way to include my entire romset and extras while only showing certain games. The tag system is a great way to acomplish this, and even easier with some prebuilt tags!

## Requirements:

* AttractMode version 1.3 or greater.

## Install Files

Tag files should be placed in the following path:

* attract/romlists/romlist/

## Usage Examples

partials from ```attract.cfg```

### neogeo

```squirrel
display	Neo Geo
	layout               mvscomplete
	romlist              neogeo
	in_cycle             yes
	in_menu              yes
	global_filter        
		rule                 Tags contains neogeo
		rule                 Category not_contains Majong
		rule                 Category not_contains Quiz
		rule                 Category not_contains Tabletop
	filter               All
	filter               Driving
		rule                 Category contains Driving
	filter               Fighter
		rule                 Category contains Fighter
	filter               Favorites
		rule                 Favourite equals 1
	filter               Maze
		rule                 Category contains Maze
	filter               Platform
		rule                 Category contains Platform
	filter               Puzzle
		rule                 Category contains Puzzle
	filter               Shooter
		rule                 Category contains Shooter
	filter               Sports
		rule                 Category contains Sports
	filter               Year
		sort_by              Year
```

### nofiller 2-player horizontal 4-button

```
display	Arcade
	layout               mvscomplete
	romlist              arcade
	in_cycle             yes
	in_menu              yes
	global_filter        
		rule                 Tags contains nofiller2p
		rule                 Rotation equals 0|180
		rule                 Buttons equals 1|2|3|4
	filter               All
	filter               Driving
		rule                 Category contains Driving
	filter               Fighter
		rule                 Category contains Fighter
	filter               Favorites
		rule                 Favourite equals 1
	filter               Maze
		rule                 Category contains Maze
	filter               Platform
		rule                 Category contains Platform
	filter               Puzzle
		rule                 Category contains Puzzle
	filter               Shooter
		rule                 Category contains Shooter
	filter               Sports
		rule                 Category contains Sports
	filter               Year
		sort_by              Year
```

## Bugs

There is currently a bug in attractmode where filtering by button count does not work due to a change in mame.xml format. It may or may not work for you. Hopefully the issue is resolved soon. See the open [issue](https://github.com/mickelson/attract/issues/420).

## Credit

### nofiller

The nofiller tag file was created based on the byoac forum topic [All Killer, No Filler MAME Gamelists Directory](http://forum.arcadecontrols.com/index.php?topic=149708.0) created by BadMouth and aided by the community.

Certain items were removed from list, such as:

* bios
* chd
* 49-way
* dual or triple screen
* speed hacks

If I happened to miss removing roms that meet the criteria from the list above, please issue a pull request or let me know so I can remove it.

Some games have variants that work better for 2 or 4 player machines. Due to this, the list was split into two different files to make it easier.

You can create a seperate tag list to include chd based games, or anything I removed that you must have. Add this seperate tag list in with your filters.