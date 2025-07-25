---
title: settings.json
description: 
published: true
date: 2025-07-25T17:48:46.167Z
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

---

### General

* `DoomsdayAnnihilationSelfDestructMode`: `false`
  Bypasses Iris’ safety checks. Only enable if you're intentionally overriding startup protections.
* `commandSounds`: `true`
  Plays a sound when commands are used.
* `debug`: `false`
  Enables verbose internal logs. Useful for deep debugging.
* `disableNMS`: `false`
  Disables usage of Minecraft’s native code (NMS). Can cause instability.
* `pluginMetrics`: `true`
  Sends anonymous usage data via bStats.
* `splashLogoStartup`: `true`
  Displays Iris' startup logo.
* `useConsoleCustomColors`: `true`
  Enables custom colors in console output.
* `useCustomColorsIngame`: `true`
  Enables custom color formatting in-game.
* `adjustVanillaHeight`: `false`
  Alters vanilla world height settings.
* `forceMainWorld`: `""`
  Forces datapacks into a custom folder. Usually left empty.
* `spinh`: `-20`, `spins`: `7`, `spinb`: `8`
  Defines gradient coloring for in-game and console visuals.
* `cartographerMessage`: `"Iris does not allow cartographers in its world due to crashes."`
  Displays when cartographers attempt to spawn or generate.

---

### World

* `asyncTeleport`:
  * `enabled`: `false` – If true, teleports & chunk generation are asynchronous.
  * `loadViewDistance`: `2` – Number of chunks (radius) to pre-load when teleporting.
  * `urgent`: `false` – When true, prioritizes the teleport request.
* `postLoadBlockUpdates`: `true`
  Runs block updates during generation for smoother runtime performance.
* `forcePersistEntities`: `true`
  Stores persistent entities in Iris’ metadata instead of querying packs.
* `anbientEntitySpawningSystem`: `true`
  Spawns mobs dynamically near players using proximity logic.
* `asyncTickIntervalMS`: `700`
  Delay (ms) between mob spawn evaluations. Higher = better performance.
* `targetSpawnEntitiesPerChunk`: `0.95`
  Global modifier for how many mobs are spawned per chunk.
* `markerEntitySpawningSystem`: `true`
  Enables spawning at designated structure markers.
* `effectSystem`: `true`
  Enables ambient particle effects (e.g., smoke, fairy dust).
* `worldEditWandCUI`: `true`
  Enables WorldEdit wand UI integration.
* `globalPregenCache`: `true`
  Enables a global cache for pregeneration data.

---
### Gui

* `useServerLaunchedGuis`: `true`
  Enables the GUI during world pregeneration, even on headless servers.
* `maximumPregenGuiFPS`: `false`
  Controls whether to maximize GUI FPS. Increases CPU usage when true.
* `colorMode`: `true`
  Enables colored GUI rendering.

---

### autoConfiguration

* `configureSpigotTimeoutTime`: `true`
  Automatically adjusts Spigot’s timeout settings.
* `configurePaperWatchdogDelay`: `true`
  Automatically adjusts Paper’s watchdog settings.
* `autoRestartOnCustomBiomeInstall`: `true`
  Restarts server automatically when a custom biome is installed.

---

### Generator

* `defaultWorldType`: `"overworld"`
  Default world preset used when no custom pack is specified.
* `maxBiomeChildDepth`: `4`
  Maximum recursion depth for biome children. Prevents infinite loops.
* `preventLeafDecay`: `true`
  Makes all leaves persistent to avoid natural decay.

---

### Concurrency

* `parallelism`: `-1`
  Thread usage:

  * `-1`: Let Iris decide
  * `-2`: Use half of available threads
  * Positive value: Use that specific number of threads

---

### Studio

* `studio`: `true`
  Enables Iris' Studio Mode for designing worlds.
* `openVSCode`: `true`
  Launches VSCode when a studio world is opened.
* `disableTimeAndWeather`: `true`
  Locks time and weather for consistent editing.
* `autoStartDefaultStudio`: `false`
  Prevents automatic loading of a studio world on startup.

---

### Performance

* `trimMantleInStudio`: `false`
  When true, uses a lighter mantle in studio for better performance.
* `mantleKeepAlive`: `30`
  Time (in seconds) to keep cached mantle data before saving.
* `cacheSize`: `4096`
  Max cache per data stream.
* `resourceLoaderCacheSize`: `1024`
  Cache size for non-script/non-object config files.
* `objectLoaderCacheSize`: `4096`
  Cache size for objects. Higher = better performance but more RAM use.
* `scriptLoaderCacheSize`: `512`
  Cache size for scripts. More = faster script parsing, more RAM use.

---

### Updater

* `threadMultiplier`: `2`
  Scales update tasks with available threads.
* `chunkLoadSensitivity`: `0.7`
  Adjusts sensitivity of chunk updates (performance vs accuracy).
* `emptyMsRange`:

  * `min`: `80`
  * `max`: `100`
    Delay range when there are no entities or chunks to update.
* `defaultMsRange`:

  * `min`: `20`
  * `max`: `40`
    Base delay range for normal update cycles.

---

### Pregen

* `useVirtualThreads`: `false`
  Use Java virtual threads (Project Loom).
* `maxConcurrency`: `256`
  Max number of concurrent generation tasks.



