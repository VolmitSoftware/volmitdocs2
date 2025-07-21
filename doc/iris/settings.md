---
title: settings.json
description: 
published: true
date: 2025-07-21T13:12:59.853Z
tags: 
editor: markdown
dateCreated: 2025-07-21T13:12:59.853Z
---

# Iris' Config File
## settings.json
```
{
    "general": {
        "DoomsdayAnnihilationSelfDestructMode": false,
        "commandSounds": true,
        "debug": false,
        "disableNMS": false,
        "pluginMetrics": true,
        "splashLogoStartup": true,
        "useConsoleCustomColors": true,
        "useCustomColorsIngame": true,
        "adjustVanillaHeight": false,
        "forceMainWorld": "",
        "spinh": -20,
        "spins": 7,
        "spinb": 8,
        "cartographerMessage": "Iris does not allow cartographers in its world due to crashes."
    },
    "world": {
        "asyncTeleport": {
            "enabled": false,
            "loadViewDistance": 2,
            "urgent": false
        },
        "postLoadBlockUpdates": true,
        "forcePersistEntities": true,
        "anbientEntitySpawningSystem": true,
        "asyncTickIntervalMS": 700,
        "targetSpawnEntitiesPerChunk": 0.95,
        "markerEntitySpawningSystem": true,
        "effectSystem": true,
        "worldEditWandCUI": true,
        "globalPregenCache": true
    },
    "gui": {
        "useServerLaunchedGuis": true,
        "maximumPregenGuiFPS": false,
        "colorMode": true
    },
    "autoConfiguration": {
        "configureSpigotTimeoutTime": true,
        "configurePaperWatchdogDelay": true,
        "autoRestartOnCustomBiomeInstall": true
    },
    "generator": {
        "defaultWorldType": "overworld",
        "maxBiomeChildDepth": 4,
        "preventLeafDecay": true
    },
    "concurrency": {"parallelism": -1},
    "studio": {
        "studio": true,
        "openVSCode": true,
        "disableTimeAndWeather": true,
        "autoStartDefaultStudio": false
    },
    "performance": {
        "trimMantleInStudio": false,
        "mantleKeepAlive": 30,
        "cacheSize": 4096,
        "resourceLoaderCacheSize": 1024,
        "objectLoaderCacheSize": 4096,
        "scriptLoaderCacheSize": 512
    },
    "updater": {
        "threadMultiplier": 2,
        "chunkLoadSensitivity": 0.7,
        "emptyMsRange": {
            "min": 80,
            "max": 100
        },
        "defaultMsRange": {
            "min": 20,
            "max": 40
        }
    },
    "pregen": {
        "useVirtualThreads": false,
        "maxConcurrency": 256
    }
}
```

`DoomsdayAnnihilationSelfDestructMode`: 
- Iris' Safe Mode bypass. Set to true to ignore Iris' warnings that prevent your server from starting.

`commandSounds`: When enabled, plays sounds when entering commands.
