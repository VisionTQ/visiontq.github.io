---
title: My OpenCode School Journey
date: 2026-07-08
categories: [opencode]
description: I completed all 14 OpenCode School lessons. Here's what I learned, what I built, and how it changed the way I work with AI.
---

I enrolled in [OpenCode School](https://opencode.school) just over a week ago. Today I finished all 14 lessons. Here is everything I learned, the tools I set up, and the skills I built along the way.

## Quick stats

- **14 lessons** completed
- **7 Replicate skills** installed
- **Brave Search MCP server** running
- **Weather MCP server** running
- **3 custom commands** (summarize, explain, start)
- **1 project skill** (Chirpy blog upgrades)
- **1 plugin** (Replicate)
- **Model used:** DeepSeek v4 Pro

## My setup before vs after

| Before | After |
|--------|-------|
| Basic installation, no config | Full `opencode.jsonc` with permissions, MCP servers, instructions URL |
| No standing instructions | `AGENTS.md` with personal preferences, MCP auth rules, GitHub rules |
| Only knew about Plan/Build | Deep understanding of agents, sessions, workspaces |
| No search capability | Brave Search MCP + built-in websearch |
| Just a ChatGPT user | Custom skills, commands, plugins, MCP servers |

## What I learned (all 14 lessons)

### Getting started
1. **Installation** — Two modes (Plan and Build), press Tab to switch. Plan thinks first, Build does the work.
2. **Interview** — OpenCode asked me about my background to personalize the course. Dabbler coder, very comfortable with terminal.

### Configuring OpenCode
3. **Configuration** — Created `~/.config/opencode/opencode.jsonc`. Set `default_agent: plan`, permissions with safety guardrails, and my school instructions URL.
4. **Permissions** — Three levels: allow, ask, deny. Added Git guardrails (`git push *: ask`, `git checkout *: ask`). Learned about per-project permission overrides.
5. **Instructions** — Created `~/.config/opencode/AGENTS.md` with my name, preferences, communication style, and rules. Config URLs vs local AGENTS.md: one fetches from a server, one lives on my machine.

### Extending OpenCode
6. **Models** — Cost vs capability tradeoff. Free Zen models vs paid flagship models. Context windows (128K-1M for big models, 8K-32K for small ones). How tokenizers work across different languages.
7. **Commands** — Custom slash commands. Created `/summarize`, `/explain` (with `$ARGUMENTS` placeholder), and `/start` (opens file explorer).
8. **Skills** — Reusable instruction packs via SKILL.md files. Installed 7 Replicate skills. Created a project skill for upgrading my Chirpy blog. [Commands vs Skills explained in detail here.](/posts/commands-vs-skills-light-switch-or-motion-sensor/)
9. **Tools** — MCP (Model Context Protocol) connects OpenCode to external tools. Added weather server (Open-Meteo). Added Brave Search MCP server. Key difference: skills are recipe books, MCP servers are working kitchens.
10. **Plugins** — JS/TS modules that hook into OpenCode's events, add custom tools, and modify behavior. Skill = advice, MCP = appliance, Plugin = remodeling. Installed Replicate plugin with 4 custom tools.

### Day-to-day use
11. **Agents** — Plan vs Build deep dive. Plan is read-only (strong guardrail, not a hard sandbox). Build has full access. Recommended workflow: Plan first, then Build.
12. **Sessions** — Each conversation is a session with its own history. Saved to disk, can resume anytime. Share via `/share`, disable for sensitive work.
13. **Images** — Vision models can interpret screenshots (UI designs, bugs, mockups, text). DeepSeek v4 Pro does NOT support vision. Claude, GPT-4/5, Gemini, Kimi K2.5 do.
14. **Workspaces** — Isolated copies of project files on their own Git branch. Desktop-only feature, so I could not use it (I use the terminal).

## What I built along the way

Throughout the lessons, I set up real tools on my machine:

- **`~/.config/opencode/opencode.jsonc`** — Global config with permissions, weather MCP, Brave Search MCP, instructions URL
- **`~/.config/opencode/AGENTS.md`** — Personal instructions with communication style, MCP auth rules, GitHub rules
- **`~/.config/opencode/commands/`** — Three custom commands
- **`~/.agents/skills/`** — Seven Replicate skills
- **`.opencode/skills/chirpy-upgrade/SKILL.md`** — Project skill for blog upgrades
- **`.opencode/plugins/replicate.ts`** — Replicate plugin
- **Brave Search API key** — 2,000 free searches/month
- **Replicate API token** — For running AI models

## What is next

The next step is exercises — hands-on projects. I have nine exercises remaining. The most practical for daily life are Git and GitHub (which I am doing right now) and Inbox Zero.

If you want to try OpenCode School yourself, enroll at [opencode.school](https://opencode.school). It is free and you can use the terminal like I did.
