---
title: Maps
date: 2026-10-23
tags: [design, maps, level]
aliases: [level design, arenas]
---

# Maps

## Design rules

- No single flat arena. Each map needs choke points, a high-ground position and a risky loot area.
- Cash opens zones (doors, bridges, shutters). A new zone also opens a new enemy spawn, so spending is a decision.
- Boss arenas are distinct spaces with their own mechanic.
- Each map has one map-specific pickup or hazard worth replaying for.

## Map 1: Research Base (year-round)

Zones in unlock order: holding cages and labs, hangar, testing ground, command bunker.

| Zone | Feature |
|---|---|
| Cages and labs | Tight corridors, apes burst from broken cages |
| Hangar | Open floor, overhead cranes, machine spawns from bays |
| Testing ground | Long sight lines, sniper high ground, mines |
| Command bunker | Boss arena for the wave-20 command mech |

## Map 2: Hollow Harvest (Halloween)

A foggy cornfield around a farmhouse and a graveyard, built for the event described in [Halloween event](05-halloween-event.md).

- Tall corn blocks sight lines. Melee weapons cut it and fire burns it, which clears space but removes cover.
- Fog thickens as waves rise.
- Spawn points are glowing pumpkins players can destroy.
- Scarecrow boss in the middle on wave 13.

## Map metadata (what the code needs per map)

Spawn points per zone, door prices, boss arena position, pickup spawns, ambient settings (lighting, fog), enemy skin set.

Related: [enemies](02-enemies.md), [UI and art](06-ui-and-art-style.md), [tech architecture](07-tech-architecture.md)
