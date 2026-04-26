# ImpulseBooster (Turtle WoW Refresh)

This is a maintained Turtle WoW refresh of Warlockbugs' original ImpulseBooster addon.

## What's updated

- Fixed the Turtle WoW white UI / whiteout issue by skipping the risky early graphics restart on Turtle-style clients by default.
- Moved the addon files to the repository root so git-based addon managers can detect the addon directly.
- Added a second root `.toc` file for installs where the folder is named `impulse-booster`.
- Restored the player's original `maxFPS` after temporary loading boosts instead of leaving the cap changed.
- Fixed IBSync cap restore behavior and the `-1` burnout watchdog edge case.
- Kept the CPU tweaks, but stopped overwriting non-default custom affinity masks.
- Retargeted the addon package to Turtle WoW's `11200` interface and cleaned up the bundled documentation.

## Turtle WoW notes

- IBSync and the extra Video Options checkboxes only work on 2.2+ clients, so they are not active on Turtle.
- If you intentionally want the old risky restart behavior back, use `/console ibAllowUnsafeRestart 1`.

## Install

### Turtle WoW Launcher / GitAddonsManager

Use this repository URL:

```text
https://github.com/Riqqqque/impulse-booster.git
```

The addon files are at the repository root for git-based addon managers. The repo includes both `impulse-booster.toc` and `!!!ImpulseBooster.toc`, so launcher installs and classic manual installs can both load the same Lua file.

### Manual Install

For the earliest possible load order, create this folder:

```text
TurtleWoW\Interface\AddOns\!!!ImpulseBooster\
```

Then place the repository files in that folder. WoW requires the addon folder name and `.toc` filename to match, so `!!!ImpulseBooster\!!!ImpulseBooster.toc` is the classic manual layout.

If you download the GitHub ZIP instead, remove any branch suffix from the extracted folder name. A folder named `impulse-booster` works with `impulse-booster.toc`; a folder named `impulse-booster-master` will not.

## Source

- Current fork: https://github.com/Riqqqque/impulse-booster
- Upstream project: https://github.com/Warlockbugs/impulse-booster
- Whiteout report: https://github.com/Warlockbugs/impulse-booster/issues/7
