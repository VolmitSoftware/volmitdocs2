---
title: Nexo Integration
description: Supporting custom nexo blocks in Iris generation.
published: true
date: 2025-11-19T12:01:55.885Z
tags: 
editor: markdown
dateCreated: 2025-11-19T09:46:40.877Z
---

Iris supports Nexo by default in any of its worlds. Assuming you have correctly configured Nexo blocks/ores to generate you will see them inside of your world upon creation. 

> If you ever see "noteblocks" in your world those are positions where Nexo ores are supposed to be but are not. When you see these this means your configuration is either incorrect or Nexo is not loaded correctly on your server. 
{.is-warning}

> Anything in [ ] (brackets) means it is interchangeable with your current pack name.
{.is-info}

## How to create custom ores

In this example we assume that you have added a block following [this example](https://docs.nexomc.com/mechanics/custom-block-mechanics/noteblock-mechanic) in Nexo.

### 1) Locate your dimension configurations

Go to `Iris/packs/[overworld]/dimensions/[overworld].json`.

Then, open the file, preferrably this should be done in [VSCode](https://code.visualstudio.com/) for Iris' integration with it.

### 2) Add your ore

> In the default overworld.json file this is located around line 230.
{.is-info}	

> If you see this: 
> `[Iris]: Failed to find BlockData! - [nexo:test_ore]`
> `[Iris]: Loading block data nexo:test_ore`
> `[Iris]: Can't find block data for nexo:test_ore`
> `[Iris]: Can't find block data for minecraft:nexo:test_ore`
> It means you have messed up your ore creation somewhere in Nexo, not Iris.
{.is-danger}

Find this part of the config:


```yml
    "deposits": [
        {
            "minHeight": 19,
            "maxPerChunk": 8,
            "maxHeight": 390,
            "minPerChunk": 1,
            "minSize": 25,
            "maxSize": 25,
            "palette": [
                {
                    "block": "minecraft:granite"
                }
            ],
            "varience": 2
        },
```

Add your own config using the custom ore properties found in step one. For example:

```yml
    "deposits": [
        {
            "minHeight": 19,
            "maxPerChunk": 8,
            "maxHeight": 390,
            "minPerChunk": 1,
            "minSize": 25,
            "maxSize": 25,
            "palette": [
                {
                    "block": "nexo:cobalt_ore"
                }
            ],
            "varience": 2
        },
```
Save the file and create a new Iris world and you're all set. 



