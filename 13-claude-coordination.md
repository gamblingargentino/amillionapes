---
title: Claude to Claude coordination
date: 2026-10-23
tags: [process, claude, team]
aliases: [coordination protocol, claim board]
---

# Claude to Claude coordination

The two Claudes cannot message each other directly. They coordinate by reading and writing shared state. Use two shared places: the vault board for plans and handoffs, and a claim board inside the Roblox place for live locks.

## 1. Vault board (slow channel, history)

File: [board](board/board.md). One section per dev.

- **Claims:** what each dev is working on and which scripts or folders they own right now.
- **Inbox:** messages for the other dev's Claude, for example "I changed the enemy table schema, re-read it before editing".
- **Handoff log:** newest first, one entry per session, using the template in [two-dev workflow](09-two-dev-workflow.md).

Sync: the vault must reach both machines. Use a shared git repo (pull before you start, commit and push when you finish) or Obsidian Sync. Without a sync, the board does nothing.

## 2. Claim board in the place (fast channel, live)

With Team Create, both Studios see the same work tree. Add a folder `WorkClaims` in ServerStorage. Each claim is a StringValue named after the script or folder, whose value is the dev name and a timestamp. Claude checks the folder before editing anything, creates a claim, and deletes it when done. Both Claudes see it within seconds.

## Rules both Claudes follow

1. Before editing: read [board](board/board.md), check `WorkClaims`, and re-read the target script.
2. If it is claimed by the other dev, do not edit it. Write an inbox message instead.
3. Claim, edit, test, release. Do not hold a claim across sessions.
4. Never rewrite a whole script file when a targeted edit works.
5. After any change to a shared table (enemies, weapons, perks), add an inbox message for the other dev.
6. Decisions go into [decisions](12-decisions-and-open-questions.md), not only chat.
7. Publish a place version before risky changes.

## Prompt to paste at the start of every session

> Read INDEX.md and board/board.md. Check the WorkClaims folder in ServerStorage. You are <Dev A or B>. Follow 13-claude-coordination.md. Before you edit any script, re-read it and claim it.

## Limits

- It is cooperative, not enforced. A Claude that ignores the board can still overwrite work, so the prompt above matters.
- Keep the humans in the loop: a quick message between devs when starting a large change beats any file.

Related: [two-dev workflow](09-two-dev-workflow.md), [Claude prompt templates](10-claude-prompts.md), [tech architecture](07-tech-architecture.md)
