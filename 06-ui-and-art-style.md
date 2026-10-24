---
title: UI and art style
date: 2026-10-23
tags: [art, ui]
aliases: [style guide, art direction]
---

# UI and art style

## Direction

Cartoon, bold and chunky. Thick outlines, saturated colours, blocky voxel-style models that read at a distance.

## UI rules

- Font: FredokaOne for headings and numbers.
- Chunky outlines on every button and panel.
- Build every screen as real instances in the Explorer (ScreenGuis authored in Studio), not as UI constructed at runtime. Scripts only show, hide and fill them.
- One accent colour per screen type: lobby, in-run HUD, results, shop.
- Keep the in-run HUD sparse: wave, boss bar, cash, abilities, health.

## Screens to author

Lobby, lobby creation, weapons, classes, titles, shop, in-run HUD, perk draft, results, event shop.

## Models

- Distinct silhouettes per enemy family: apes are hunched and wide, machines are boxy and angular, hybrids show both shapes.
- Hybrids use a shared set of plating and drone pieces so new hybrids are cheap to assemble.
- Bosses are two to three times the size of normal enemies with one glowing weak point.

## Audio

Distinct sound per enemy family, a rising music layer per wave range, a stinger when a boss spawns.

Related: [enemies](02-enemies.md), [maps](04-maps.md), [tech architecture](07-tech-architecture.md)
