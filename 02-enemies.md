---
title: Enemies and waves
date: 2026-10-23
tags: [design, enemies]
aliases: [enemy ladder, wave design]
---

# Enemies and waves

Theme: apes experimented on in a military base fuse with leftover war machines. Three families, then hybrids that combine their rules.

## Wave ladder

| Waves | Family | Role | Examples |
|---|---|---|---|
| 1-5 | Apes | Fast, weak, many | Chimp, baboon |
| 6-10 | Machines | Slower, tankier, some ranged | Scout drone, walker bot |
| 11-20 | Hybrids | Mix both rule sets | Armoured gorilla (front plating), ape with drone on its back (jump then fire), walker with ape pilot (kill the pilot to stop it) |
| 21+ | Experiments | Large, one clear weak point | Fused beast with exposed core |

Bosses: wave 10 giant armoured gorilla; wave 20 command mech with an ape brain that buffs nearby enemies.

## Why hybrids work

Players learn the apes and the machines first. Hybrids then reuse both rules, so skill carries over and each new threat is still readable.

## Wave director (budget system)

Each wave gets a budget of points. Each enemy type has a point cost and a first wave it can appear. The director picks types by weight until the budget is spent.

- Budget grows each wave, and the weights shift toward costlier types.
- Cap simultaneous enemies (start at 80) to protect server performance. Excess spawns wait.
- Boss waves reserve part of the budget for the boss and its escorts.

Starting scaling (tune in playtests):

- Enemy health grows about 8 to 12 percent per wave.
- Speed stays almost flat so waves stay readable.
- Damage grows slowly. Counts do most of the escalation.

## Enemy spec template

Every enemy gets one entry with: family, role, health multiplier, speed, attack, first wave, point cost, weak point (if any), model silhouette note, drop table.

Related: [vision](00-vision.md), [maps](04-maps.md), [tech architecture](07-tech-architecture.md), [Halloween event](05-halloween-event.md)
