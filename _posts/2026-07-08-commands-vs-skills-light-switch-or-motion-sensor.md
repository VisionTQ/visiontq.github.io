---
title: "Commands vs Skills: Light Switch or Motion Sensor?"
date: 2026-07-08
categories: [opencode]
description: Both give instructions to OpenCode, but they work in completely different ways. Here's when to use each one.
hidden: true
---

When I first learned about commands and skills in OpenCode, they seemed like the same thing to me. Both give the AI instructions. Both make it smarter. So why do both exist?

Here's how I think about it.

A command is a button you press. A skill is a sensor that triggers on its own.

## Commands = a light switch

You type `/something`. It runs. You're in control.

A command is just a shortcut. Instead of typing the same long prompt every time, you save it once and run it with a few keystrokes.

Commands I actually use:
- `/summarize` — gives me a quick overview of whatever project I'm working on
- `/explain git push` — explains something in plain language (the `$ARGUMENTS` part fills in whatever I type after `/explain`)
- `/start` — opens my file explorer so I don't have to leave the terminal

When a command makes sense:
- You want a shortcut you control
- The task is simple, one-and-done
- You know exactly when you want it to fire

## Skills = a motion sensor

You just talk normally. The AI reads the skill's description, matches it to what you said, and loads the instructions on its own. No slash needed, no typing anything special.

A skill is knowledge you give the AI. It sits in the background and only wakes up when it's relevant.

Skills I use:
- Chirpy blog upgrade — when I say "upgrade my blog," it loads a full step-by-step procedure. Before this skill, I had to remember every step or dig through my notes.
- Replicate skills — seven skills for AI model stuff (finding, comparing, running, publishing). They trigger when I mention image generation or video models.

When a skill makes more sense:
- The task is complex (multiple steps, edge cases)
- You want the AI to just know something without being told
- You might forget the exact procedure
- You want it to work across different AI tools (Claude Code, Codex, Cursor all support the skills format)

## Quick rule of thumb

| If you think... | Then use... |
|-----------------|-------------|
| "I want to push a button" | Command |
| "The AI should figure it out on its own" | Skill |
| Simple, one-shot task | Command |
| Multi-step workflow with edge cases | Skill |
| I want to control exactly when it fires | Command |
| I want it to work in other AI tools too | Skill |

## Where they live

Commands: `~/.config/opencode/commands/`. One markdown file per command. The filename is the command name. Simple.

Skills: `~/.agents/skills/` (global, available everywhere) or `.opencode/skills/` (per project). Each skill gets its own folder with a `SKILL.md` file inside.

## Why both exist

Commands are for things you do on purpose. Skills are for things the AI should just know.

Real example: my Chirpy upgrade skill. If I turned it into a `/upgrade-chirpy` command, I'd have to remember it exists and type it exactly that way. If someone else opened my project, they'd never know it's there.

As a skill, it just works. I say "I need to upgrade my blog" and OpenCode loads the whole procedure automatically. That's the difference.

A command is a light switch. You flip it on purpose.

A skill is a motion sensor. It triggers when you walk into the room.
