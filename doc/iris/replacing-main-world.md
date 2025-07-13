---
title: Replacing Your Main World
description: 
published: true
date: 2025-07-13T15:22:36.210Z
tags: 
editor: markdown
dateCreated: 2025-07-13T14:19:14.584Z
---

# Replacing your Main World

> While issues are unlikely, setting Iris as your main world while using other unsupported world generators will cause world corruption. Unsupported plugins and datapacks include: Terra, EpicWorldGenerator, Terralith.
{.is-danger}

> Have a question on if your datapack or plugin is supported? Contact us on [Discord](https://discord.gg/yk3F6enprh).
{.is-info}

## Preparation

To replace your main world make sure you have:
- Opened your Spigot/Paper server folder.
- Opened your `server.properties` file.
![iris_replace2.png](/iris_docs/iris_replace2.png)
# Beginning

- Create your iris world using the command given in the [Creating your Iris World](/doc/iris/create-world) page.
- Once the creation has finished, stop your server.
- Open your `server.properties` file and find the option containing the `level-name` parameter.
- Change this from `world` to the current name of your Iris world.
