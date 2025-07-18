---
title: Mythic Mobs
description: 
published: true
date: 2025-07-18T19:04:11.465Z
tags: 
editor: markdown
dateCreated: 2025-07-18T18:48:10.450Z
---

# MythicMobs Integration
> Support is exclusive to MythicMobs 5 and above. If you have an older version this wiki may be inaccurate.
{.is-info}

- [Download MythicMobs Here](https://mythiccraft.io/index.php?pages/official-mythicmobs-download/&version=4.12.0)
{.links-list}

## Iris Entities

> You can spawn mythic mobs in custom biomes by following this format. View a larger explanation via [Entities](/doc/iris/entities-spawners-markers).
{.is-info}

```
{
    "type": "CAT",
    "surface": "LAND",
    "specialType": "MythicMobs:JumpingSpider"
}
```

> The "type": "CAT" does not actually change anything. It just makes sure Iris accepts the entity.

As seen here, to make Iris spawn a mythic mob, you'll need to create a new Iris entity file with specialType, where you prefix the name with MythicMobs: 

> VSCode will autocomplete names installed on the server if you are using [Iris Studio](/doc/iris/iris-studio), too!

# MythicMobs RandomSpawns
See the MythicMobs wiki:
 
- [Skills -> Conditions](https://git.mythiccraft.io/mythiccraft/MythicMobs/-/wikis/Skills/conditions/)
{.links-list}

More specifically:
- [Skills -> Conditions -> Biomes](https://git.mythiccraft.io/mythiccraft/MythicMobs/-/wikis/Skills/conditions/biome)
{.links-list}