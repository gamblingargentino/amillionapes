---
title: Tech architecture
date: 2026-10-23
tags: [tech, roblox]
aliases: [architecture, systems]
---

# Tech architecture

## Server-authoritative services

| Service | Job |
|---|---|
| WaveDirector | Budget-based spawning, boss waves, wave-skip vote |
| EnemyService | Spawn, pooling, chase behaviour, weak points, drops |
| WeaponService | Validates hits on the server, damage and fire rate |
| EconomyService | Cash for the current run |
| PerkService | Draft offers and active perks |
| DataService | Gems, XP, owned weapons, classes, titles (saved data) |
| LobbyService | Pads, lobby size, public or private, teleport into runs |
| EventService | Reads the event config and switches skins and shops |

Clients only render and send input. Never trust the client for damage or currency.

## Performance budget

- Cap live enemies (start at 80) and queue the rest.
- Simple chase for normal enemies. Use pathfinding only for large ones.
- Pool and reuse enemy models, and remove enemies stuck far from players.
- Keep models low part-count and anchored where possible.
- Test with four players and a full wave on a low-end device early.

## Project setup for two devs

- Use Rojo plus git so scripts live as files and merge cleanly. Keep the place file for map and UI assets only.
- Split by folder ownership (see [two-dev workflow](09-two-dev-workflow.md)) so two people rarely edit the same file.
- UI lives in the place file as real instances. Only scripts live in git.
- No code comments. Names carry the meaning.

## Suggested folder layout

- `src/server/` services above
- `src/client/` HUD, input, effects
- `src/shared/` config, enemy and weapon tables, constants
- Data tables for enemies, weapons, classes, perks and maps live in `src/shared/` so balance changes need no code edits.

Related: [enemies](02-enemies.md), [core loop](01-core-loop.md), [roadmap](08-roadmap.md)
