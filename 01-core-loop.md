---
title: Core loop and economy
date: 2026-10-23
tags: [design, economy]
aliases: [game loop, progression]
---

# Core loop and economy

## One run

1. Squad picks a map and lobby size in the lobby, then deploys.
2. A wave spawns. Kills pay **cash** (run-only).
3. Between and during waves, cash buys health, weapons, abilities and zone unlocks.
4. Every few waves a **perk draft** offers three choices.
5. A boss appears on a fixed wave interval (see [enemies](02-enemies.md)).
6. The run ends on squad wipe. The results screen pays **XP** and **gems** (permanent).

## Two economies

| Currency | Earned | Spent on | Resets |
|---|---|---|---|
| Cash | Kills, wave clears | In-run upgrades, weapons, abilities, zone doors | Every run |
| Gems | End of run, scaled by waves, kills, bosses, new best | Weapon tiers and star upgrades, classes | Never |
| XP | End of run | Account level, unlocks | Never |

Starting numbers below are taken from what the reference game charges. Treat them as placeholders to tune in playtests.

| Item | Placeholder |
|---|---|
| Health upgrade | 10 cash, repeatable |
| Shotgun purchase | 150 cash |
| Grenade ability | 50 cash |
| Barricade ability | 40 cash |
| Weapon star upgrade | 750 to 1,250 gems at the first levels |
| Class unlock | 15,000 to 300,000 gems, rarer is pricier |

## Pacing targets

- About 60 to 90 seconds per wave early on, so wave 20 lands near 20 to 25 minutes.
- A boss gate every 10 waves gives a goal for the run.
- A wave-skip vote (all players must agree) lets squads speed up easy waves.

## Meta goals that keep players returning

- Weapon tiers 1 to 4, each with star upgrades.
- Class ladder with one legendary class.
- Titles for milestones such as kill counts, wave 50 and wave 100, boss kills, and runs with friends.
- Leaderboards for highest wave and most kills.

Related: [vision](00-vision.md), [classes and weapons](03-classes-and-weapons.md), [monetization](11-monetization-and-live-ops.md)
