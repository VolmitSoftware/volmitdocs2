---
title: Create a new world with Iris
description: 
published: true
date: 2025-07-13T15:09:27.313Z
tags: 
editor: markdown
dateCreated: 2025-07-13T13:24:16.611Z
---

# How to Create a World

Iris allows you to generate stunning custom worlds with unique terrain, biomes, and structures. Follow this guide to create and manage your own dimension.  



## Preparation  
Before beginning, ensure you have:  
- ✅ **Iris installed** on your Spigot/Paper server. Grab the latest jar from [Spigot](https://www.spigotmc.org/resources/iris-world-gen-the-dimension-engine.84586/), [BuiltByBit](https://builtbybit.com/resources/iris-dimension-engine.56258/?ref=discover), or [Polymart](https://polymart.org/product/3623/iris-dimension-engine).
- ✅ **Sufficient RAM** (at least 6GB recommended for large worlds).  
- ✅ **Proper permission manager**: We recommend [LuckPerms](https://luckperms.net/).
- ✅ **Proper permissions** (OP or `iris.world.create` permission).  

> Do not give yourself the `iris.*` or `*` permission, as this can cause conflicts.
{.is-warning}


# Beginning
- Once you have installed the Iris plugin, by placing the jar file downloaded in the previous step, start your server.
- Once your server has started, Iris will begin downloading libraries and iris content. During this process it will restart your server.
- Verify the `Custom Biomes` in the console reads `>70`.
![image.jpg](/iris_docs/image.jpg)

> Is your server constantly restarting or the biome amount reads 0? Contact us on our [Discord](https://discord.gg/yk3F6enprh).
{.is-info}

# Creating a World
Use `/iris create`.

> Writing the parameters in this command are case sensitive. All parameters should be lowercase when running the command.
{.is-warning}

- Parameters (required):
 `Name` | /iris create name=iris
 `Type` | /iris create type=overworld
- Parameters (optional):
 `Seed` | /iris create seed=1337

Example:
`/iris create name=iris type=overworld seed=1337`



# Accessing the World
You can access your world by running `/iris tp world=<name>`.



- [Next *Replacing Your Main World*](/doc/iris/replacing-main-world)
{.links-list}
