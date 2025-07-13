---
title: Replacing Your Main World
description: 
published: true
date: 2025-07-13T16:14:41.098Z
tags: 
editor: markdown
dateCreated: 2025-07-13T14:19:14.584Z
---

# Replacing your Main World

> While issues are unlikely, setting Iris as your main world while using other unsupported world generators **will** cause world corruption. Unsupported plugins and datapacks include: Terra, EpicWorldGenerator, Terralith.
{.is-danger}

> Have a question on if your datapack or plugin is supported? Contact us on [Discord](https://discord.gg/yk3F6enprh).
{.is-info}

## Preparation

To replace your main world make sure you have:
- Opened your Spigot/Paper server folder.
- Opened your `server.properties` file.

# Beginning

- Create your iris world using the command given in the [Creating your Iris World](/doc/iris/create-world) page.
- Once the creation has finished, stop your server.
- Open your `server.properties` file and find the option containing the `level-name` parameter.
- Change this from `world` to the current name of your Iris world.
![iris_replace2.png](/iris_docs/iris_replace2.png)
- Return to your server folder.
- Open your `world` folder and copy the folder `datapacks`. Move this folder into your iris world folder (in this case `iris`) and paste the folder there.
- Delete the `world`, `world_nether`, and `world_the_end` as they are no longer used.
- Start your server and a new `iris_nether` and `iris_the_end` will be created.

Once you have finished these steps, you have successfully set Iris as your main world.

- [Next *Command Usage*](/doc/iris/commands)
{.links-list}

