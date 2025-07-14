---
title: Command Usage
description: 
published: true
date: 2025-07-14T12:54:51.261Z
tags: 
editor: markdown
dateCreated: 2025-07-13T15:59:22.969Z
---

# Command Usage
> Here will include a list of all Iris commands that you may need to know. If a command is too long for this page, it will be placed on a new page linked underneath it.
{.is-info}

> Hover over commands in chat to see their descriptions.
{.is-info}

# Iris
Aliases: `irs`, `ir`, `iris`
The top level argument for all Iris commands.

```
/iris
```

## Aura

Aliases: `aura`
Set aura spin.

* `h`
  The h color value.
* `s`
  The s color value.
* `b`
  The b color value.

```
/iris aura h=0.5 s=1.0 b=0.8
```

## Bitwise

> Perform bitwise calculations between two integer values.
> {.is-info}

Aliases: `bitwise`
Performs various bitwise operations on two integer values.

* `value1`
  The first value to run calculations on.
* `operator`
  The bitwise operator: `|` (OR), `&` (AND), `^` (XOR), `<<` (left shift), `>>` (right shift), or `%` (modulo).
* `value2`
  The second value to run calculations on.

```
/bitwise 5 & 3
```

```
/bitwise 4 << 1
```

```
/bitwise 7 ^ 2
```

## Create

Aliases: `c`, `+`, `create`
Create a new Iris world.

* `name`
  The name you want for your Iris world.
* `type`
  Which dimension pack Iris should use to create this world.
* `seed`
  The seed Iris should use to create this world.

```
/iris create name=<my_world> type=overworld seed=1337
```

## Debug

Aliases: `debug`
Toggle the debug information in Console.

* `on`
  A true or false variable to turn debug on and off.

```
/iris debug on/off
```

## Download

Aliases: `dl`, `download`
Download a project.

* `pack`, `project`
  The pack to download.
* `branch`
  Which version to use.
* `trim`
  Whether or not to use a trimmed version.
* `overwrite`, `force`
  Whether or not to overwrite the existing pack with the one being downloaded.

```
/iris download pack=overworld branch=master trim=true/false overwrite=true/false
```

## Edit

Aliases: `edit`
Edit something.
`region`, `r`
Edit the region you specify.
`dimension`, `d`
Edit the dimension you specify.
`biome`, `b`
Edit the biome you specify.
`jigsaw`, `pool`, `jigsawpool`
Edit the pool file you specify.
`cave`, `c`
Edit the cave file you specify.
`jigsawPiece`, `piece`
Edit the jigsaw pieces you specify.

```
/iris edit region region=frozen
```

## Evacuate

Kick everyone out of an Iris world.

* `world`
  The world name to remove players from.

```
/iris evacuate <my_world>
```

## Find

Aliases: `find`, `goto`
Find something.
`object`
Find an object.
`region`
Find a region.
`biome`
Find a biome.
`structure`
Find a structure.
`poi`
Find a point of interest.

```
/iris find structure structure=village-savanna
```

## Height

Aliases: `height`
Prints the current world height information.

```
/iris height
```

## Jigsaw

Aliases: `jigsaw`
Iris jigsaw commands.
Subcommands:
`place`
Place a jigsaw structure.

* `structure`
  A jigsaw structure to place.

`exit`
Exit the current jigsaw editor.
`save`
Save and Exit the current jigsaw editor.
`create`
Create a jigsaw piece.

* `piece`
  The name of a jigsaw piece.
* `project`
  The project to add the jigsaw piece to.
* `object`
  The object to use for this piece.

`edit`
The jigsaw piece to edit.

```
/iris jigsaw place structure=igloo
```

## LoadWorld

Aliases: `loadWorld`

* `world`
  The world to load.

```
/iris loadWorld world=<my_world>
```

## Metrics

Aliases: `metrics`
Get the current Metrics for your world.

```
/iris metrics
```

## Object

Aliases: `o`, `object`
Top argument for Iris Object manipulation.

```
/iris object
```

* [Object *Iris Object Command Arguments*](/doc/iris/object-commands)
  {.links-list}

## Pregenerate

Aliases: `pregen`, `pregenerate`
Iris' built-in Pregeneration.
Subcommands:
`start`

* `radius`
  Set the Radius for the pregeneration in blocks.
* `world`
  Set the world you wish to pregenerate.
* `center`
  Choose the XY coordinates where you wish to start the pregeneration. Use "me" for current location. Defaults to "0,0" if unset.

`stop`, `x`
Stop the active pregeneration.
`pause`
Pause the active pregeneration.

```
/iris pregen start radius=5000 world=<my_world> center=0,0
```

## Reload

Aliases: `reload`
Reload the configuration files.

```
/iris reload
```

## Remove

Aliases: `delete`, `rm`, `del`, `remove`
Remove an Iris world.

* `world`
  Select the world you want to remove.
* `delete`
  Whether or not to delete the world from the server. (default: true)

```
/iris remove world=<my_world> delete=true/false
```

## Studio

Aliases: `s`, `std`, `studio`
Top argument for Iris Studio.

```
/iris studio
```

* [Studio *Iris Studio Command Arguments*](/doc/iris/studio-commands)
  {.links-list}

## Teleport

Aliases: `teleport`, `tp`
Teleport to an Iris world.

* `world`
  Which world to teleport to.
* `player`
  The player to teleport to the Iris world.

```
/iris teleport world=<my_world> player=<player_name>
```

## UnloadWorld

Aliases: `unloadWorld`
Unload an Iris world.

* `world`
  Which world to unload.

```
/iris unloadWorld world=<my_world>
```

## Updater

Aliases: `updater`
Updates all chunks in the specified world.

* `world`
  World name to update chunks.

```
/iris updater world=<my_world>
```

## Version

Aliases: `version`
Print the plugins current version information.

```
/iris version
```

## What

Aliases: `what`
Identify a Block, Item, Region, Biome.
Subcommands:
`markers`
Show markers in Chunk.

* `marker`
  Marker such as `cave_floor` or `cave_ceiling`.

`block`
Identify what I'm looking at.
`region`
Identify the current Region.
`biome`
Identify the current Biome.
`hand`
Identify what's in my hand.

```
/iris what block
```

## Worlds

Aliases: `accesslist`, `world`
Access a list of all Iris worlds.

```
/iris world
```

## ^world

> An extremely unsafe command. Only do this if staff or your pack developer says so.
> {.is-warning}

Aliases: `update-world`, `^world`
Updating the pack of an Iris world.

* `world`
  The world to update.
* `dimension`, `pack`
  The updated version to install in place of the old pack.
* `c`, `confirm`
  A required confirmation that you want to proceed.
* `fresh`, `new`, `new-download`
  Should Iris download the pack again for you.

```
/iris ^world <my_world> dimension:new_pack_version confirm:true
```

