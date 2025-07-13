---
title: Command Usage
description: 
published: true
date: 2025-07-13T16:30:58.804Z
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

