---
title: Two-dev workflow with two Claude subscriptions
date: 2026-10-23
tags: [process, team, claude]
aliases: [team workflow, ownership]
---

# Two-dev workflow with two Claude subscriptions

Each dev works with their own Claude. This vault is the shared memory both Claudes read at the start of a session, so neither has to be re-briefed.

## Ownership split (suggested, swap to fit skills)

| Area | Dev A (systems) | Dev B (world and UI) |
|---|---|---|
| Wave director, enemy AI, weapons, economy, data | Owner | Reviews |
| Maps, lighting, spawn points, boss arenas | Reviews | Owner |
| UI screens, HUD, art, models, audio | Reviews | Owner |
| Enemy and weapon data tables | Shared, one editor at a time | Shared |

Rule: one owner per file or folder. Anyone else asks the owner or proposes a change.

## Daily rhythm

1. Start: read [INDEX](INDEX.md) and the notes for your task. Check the open questions note.
2. Work in small tasks that end in something testable.
3. End: write a handoff note (template below), update decisions, push.

## Using two Claudes well

- Each dev keeps their own Claude sessions. Do not assume one Claude knows what the other did. Use the vault and git history.
- Give every session one task and the notes it needs, not the whole library.
- Save heavy work (big refactors, bulk content generation) for the start of a usage window, and use light work to fill the rest.
- Write decisions into [decisions](12-decisions-and-open-questions.md), not just into chat.
- Prompt templates are in [Claude prompts](10-claude-prompts.md).

## Handoff note template

Task, what changed (files), how to test it, what is broken or unfinished, next step, who owns it.

## Merge rules

- Small commits, rebase before you push.
- No two people edit the same script file in the same hour.
- The place file has one editor at a time. Announce before opening it.

Related: [tech architecture](07-tech-architecture.md), [roadmap](08-roadmap.md), [Claude prompts](10-claude-prompts.md)
