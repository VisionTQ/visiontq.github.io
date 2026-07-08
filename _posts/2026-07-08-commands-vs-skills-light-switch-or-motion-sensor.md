---
title: "Commands vs Skills: Light Switch or Motion Sensor?"
date: 2026-07-08
categories: [opencode]
description: Both give instructions to OpenCode, but they work in completely different ways. Here is when to use each one.
---

When I first learned about commands and skills in OpenCode, they seemed like the same thing. Both give the AI instructions. Both make it smarter. So why do both exist?

Here is the simple answer.

## The difference in one sentence

A **command** is a button you press. A **skill** is a sensor that triggers on its own.

## Commands = a light switch

You type `/something`. It runs. You are in control.

A command is a shortcut. Instead of typing a long prompt every time, you save it once and run it with a few keystrokes.

**What I use commands for:**
- `/summarize` — gives me an overview of the current project
- `/explain git push` — explains something in layman's terms (using the `$ARGUMENTS` placeholder to fill in whatever I need)
- `/start` — opens my file explorer in the current directory

**When to use a command:**
- You want a shortcut you control
- The task is one-and-done (no multi-step logic)
- You know exactly when you want it to fire
- You want to push a button, not rely on the AI figuring it out

## Skills = a motion sensor

You talk normally. The AI reads the skill's description, matches it to what you said, and loads the full instructions automatically. No slash needed.

A skill is knowledge you give the AI. It sits in the background and only activates when relevant.

**What I use skills for:**
- **Chirpy blog upgrade** — triggers when I say "upgrade my blog." Contains a full 7-step procedure with submodule handling and version-specific logic.
- **Replicate skills** — seven skills for finding, comparing, running, and publishing AI models. They trigger when I mention image generation or video models.

**When to use a skill:**
- The task is complex (multiple steps, edge cases)
- You want the AI to just know something without being told
- You might forget the exact procedure
- You want it to work across different AI tools (Claude Code, Codex, Cursor all support the skills format)

## Quick rule of thumb

| Question | Answer |
|----------|--------|
| "Do I want to push a button?" | Use a command |
| "Should the AI figure it out on its own?" | Use a skill |
| Simple one-shot task? | Command |
| Multi-step workflow with edge cases? | Skill |
| I want to control exactly when it fires? | Command |
| I want it to work in other AI tools too? | Skill |

## Where they live on my machine

Commands are in `~/.config/opencode/commands/`. One markdown file per command. The filename becomes the command name.

Skills are in `~/.agents/skills/` (global) or `.opencode/skills/` (per project). Each skill has its own folder with a `SKILL.md` file inside.

## Why both exist

Commands are for things you do on purpose. Skills are for things the AI should just know.

If I turned my Chirpy upgrade skill into a `/upgrade-chirpy` command, I would have to remember it exists and type it exactly. If someone else used my project, they would never know it is there.

As a skill, it just works when I say "I need to upgrade my blog." That is the difference.
