---
title: Claude prompt templates
date: 2026-10-23
tags: [claude, prompts, process]
aliases: [session starters]
---

# Claude prompt templates

Paste one of these at the start of a session. Replace the angle-bracket parts.

## Session start

> Read INDEX.md, then <note names>. I am <Dev A or Dev B> and I own <folders>. Task: <one task>. Constraints: no code comments, UI built as real instances in the Explorer, server decides damage and currency. Tell me your plan in five lines before you change anything.

## Build a system

> Using 02-enemies.md and 07-tech-architecture.md, implement <service>. Put data in src/shared tables. Give me a way to test it with one player. List the files you changed.

## Review the other dev's work

> Review the changes in <files>. Check server authority, performance with 80 enemies, and whether the data tables still match 02-enemies.md. Report problems only.

## Balance pass

> Read 01-core-loop.md and 02-enemies.md. Simulate waves 1 to 30 with the current tables and list where cash income or enemy health breaks pacing.

## Handoff

> Write a handoff note for what we did this session using the template in 09-two-dev-workflow.md, and list any decision that should go into 12-decisions-and-open-questions.md.

Related: [two-dev workflow](09-two-dev-workflow.md), [tech architecture](07-tech-architecture.md)
