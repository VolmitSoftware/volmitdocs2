---
title: Command Usage
description: 
published: true
date: 2025-07-14T11:50:11.362Z
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
Aliases: `irs` `ir` `iris`
The top level argument for all Iris commands.


# Studio
Aliases: `s` `std` `studio`
Top argument for Iris Studio.
- [Studio *Iris Studio Command Arguments*](/doc/iris/studio-commands)
{.links-list}

# Object
Aliases: `o` `object`
Top argument for Iris Object manipulation.
- [Object *Iris Object Command Arguments*](/doc/iris/object-commands)
{.links-list}

# Pregenerate
Aliases: `pregen` `pregenerate`
Iris' built-in Pregeneration.
Subcommands: 
`start`
- `radius`
Set the Radius for the pregeneration in blocks.
- `world`
Set the world you wish to pregenerate.
- `center` 
Choose the XY coordinates where you wish to start the pregeneration. Use "me" for current location. Deaults to "0,0" if unset.

 `stop`, `x`
Stop the active pregeneration.
 `pause`
Pause the active pregeneration.

# Jigsaw
Aliases: None
Iris jigsaw commands.
Subcommands:
`place`
Place a jigsaw structure.
- `structure`
A jigsaw structure to place.

`exit`
Exit the current jigsaw editor.
`save`
Save and Exit the current jigsaw editor.
`create`
Create a jigsaw piece.
- `piece`
The name of a jigsaw piece.
- `project`
The project to add the jigsaw piece to.
- `object`
The object to use for this piece.

`edit`
The jigsaw piece to edit.

# What
Aliases: `what`
Identify a Block, Item, Region, Biome.
Subcommands:
`markers`
Show markers in Chunk.
- `marker`
Marker such as `cave_floor` or `cave_ceiling`.

`block`
Identify what I'm looking at.
`region`
Identify the current Region.
`biome`
Identify the current Biome.
`hand`
Identify what's in my hand.

# Edit 
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

# Find
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

# Download
Aliases: `dl`, `download`
Download a project.
- `pack`, `project`
 The pack to download.
- `branch` 
 Which version to use.
- `trim`
 Whether or not to use a trimmed version.
- `overwrite`, `force`
 Whether or not to overwrite the existing pack with the one being downloaded.

# Remove
Aliases: `delete`, `rm`, `del`, `remove`
Remove an Iris world.
- `world`
 Select the world you want to remove.
- `delete`
 Whether or not to delete the world from the server. (default: true)

# Reload
Aliases: `reload`
Reload the configuration files.

# Metrics
Aliases: `metrics`
Get the current Metrics for your world.

# Version
Aliases: `version`
Print the plugins current version information.

# Debug
Aliases: `debug`
Toggle the debug information in Console.
- `on` 
A true or false variable to turn debug on and off.

# Create
Aliases: `c`, `+`, `create`
Create a new Iris world.
- `name`
The name you want for your Iris world.
- `type`
Which dimension pack Iris should use to create this world.
- `seed`
The seed Iris should use to create this world.



# Updater
Aliases: `updater`
Updates all chunks in the specified world.
- `world`
World name to update chunks.

