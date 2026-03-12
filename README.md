# ImpulseBooster (Turtle WoW Refresh)

This is a maintained Turtle WoW refresh of Warlockbugs' original ImpulseBooster addon.

## What's updated

- Fixed the Turtle WoW white UI / whiteout issue by skipping the risky early graphics restart on Turtle-style clients by default.
- Restored the player's original `maxFPS` after temporary loading boosts instead of leaving the cap changed.
- Fixed IBSync cap restore behavior and the `-1` burnout watchdog edge case.
- Kept the CPU tweaks, but stopped overwriting non-default custom affinity masks.
- Retargeted the addon package to Turtle WoW's `11200` interface and cleaned up the bundled documentation.

## Turtle WoW notes

- IBSync and the extra Video Options checkboxes only work on 2.2+ clients, so they are not active on Turtle.
- If you intentionally want the old risky restart behavior back, use `/console ibAllowUnsafeRestart 1`.

## Install

Copy the `!!!ImpulseBooster` folder into your client's `Interface\AddOns\` directory.

## Source

- Current fork: https://github.com/Riqqqque/impulse-booster
- Upstream project: https://github.com/Warlockbugs/impulse-booster
- Whiteout report: https://github.com/Warlockbugs/impulse-booster/issues/7
