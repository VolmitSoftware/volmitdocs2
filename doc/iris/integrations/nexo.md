---
title: Nexo Integration
description: Supporting custom nexo blocks in Iris generation.
published: true
date: 2025-11-20T00:55:32.540Z
tags: 
editor: markdown
dateCreated: 2025-11-19T09:46:40.877Z
---

# Nexo Integration

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
```json
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
```json
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

### 3) Optional: Protect specific blocks from replacement

If you want to prevent certain blocks from being replaced by ore deposits (for example, to protect Nexo custom blocks or other special blocks), you can use the `varianceBlocklist`:

```json
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
            "varience": 2,
            "varianceBlocklist": [
                "nexo:custom_stone",
                "nexo:special_block"
            ]
        },
```

The `varianceBlocklist` accepts a list of block IDs that should never be replaced when the ore deposit generates. This is useful for:
- Protecting custom Nexo blocks from being overwritten
- Preserving specific vanilla blocks in certain areas
- Preventing ores from replacing important structural blocks

Save the file and create a new Iris world and you're all set.

---

## Custom Furniture Block Options

When placing Nexo furniture blocks in your Iris world generation, you can use additional data options to control their appearance and behavior:

**matchBiome** - Match the block's color to the biome's natural colors:
- `FOG` - Match biome fog color
- `WATER` - Match biome water color
- `WATER_FOG` - Match biome water fog color
- `SKY` - Match biome sky color
- `FOLIAGE` - Match biome foliage color
- `GRASS` - Match biome grass color

**randomFace** (default: `false`) - Randomly orient the block's facing direction:
- `true` - Random facing direction
- `false` - Use specified face

**face** (default: `NORTH`) - Set a specific facing direction:
- `NORTH`, `NORTH_EAST`, `NORTH_NORTH_EAST`
- `EAST`, `EAST_SOUTH_EAST`, `SOUTH_EAST`, `SOUTH_SOUTH_EAST`
- `SOUTH`, `SOUTH_SOUTH_WEST`, `SOUTH_WEST`, `WEST_SOUTH_WEST`
- `WEST`, `WEST_NORTH_WEST`, `NORTH_WEST`, `NORTH_NORTH_WEST`
- `UP`, `DOWN`

**randomYaw** (default: `false`) - Randomly rotate the block:
- `true` - Random rotation
- `false` - Use specified yaw

**yaw** (default: `0`) - Set a specific rotation angle (0-360 degrees)

### Example Usage

```json
{
    "chance": 0.02,
    "variance": {"style": "STATIC"},
    "zoom": 0.2,
    "palette": [{
        "block": "nexo:plant_1",
        "data": {
            "matchBiome": "GRASS",
            "randomYaw": "true",
            "randomFace": "true"
        }
    }]
}
```

This example creates a plant that:
- Matches the grass color of the biome it generates in
- Has a random rotation (yaw)
- Has a random facing direction
- Has a 2% chance to spawn per eligible block
