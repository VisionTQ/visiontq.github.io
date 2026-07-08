---
title: My OpenCode School Journey
date: 2026-07-08
categories:
  - opencode
description: I completed all 14 OpenCode School lessons. Here's what I learned, what I built, and how it changed the way I work with AI.

---

Friday, June 26, 6 AM

Getting Started:
The guide will be using the desktop app for OpenCode. I will be using the terminal since that's what I'm used to. The OS I will be using is Linux Mint.

First Lesson:
I'm on Linux and to open the terminal, I clicked Ctrl + Alt + T and then moved to the directory or project file I'm going to work on, then after that type opencode.


in the first lesson I learned that there are 2 modes or as they call it "agents" when I press the tab key it switches from plan & build. 

I think they are self explanatory but plan means "think through it first" before changing anything and build is just do it mode.

https://opencode.school/lessons/installation/

---

Second Lesson: Interview

The agent asked me questions about:
- Coding experience: Dabbler (tinkered a bit)
- AI tools used: ChatGPT, Gemini, Claude
- Editor: None yet
- Terminal comfort: Very comfortable
- Learning style: Flexible (all approaches)
- Detail preference: Some context

The agent auto-detected my OS as Linux and saved my profile to the OpenCode School API. This profile will personalize future lessons.

https://opencode.school/lessons/interview/

---

Third Lesson: Configuration

Set up the global OpenCode config at ~/.config/opencode/opencode.jsonc. The agent backed up my existing config first.

What we added:
- default_agent: "plan" — every session starts in read-only Plan mode
- Permissions: most actions auto-allowed, destructive commands (rm, rmdir) prompt first
- Instructions URL so OpenCode always knows my school profile

The agent noted my existing config was minimal (just $schema) and used surgical edits to add missing keys instead of overwriting. Had to restart OpenCode for changes to take effect.

https://opencode.school/lessons/configuration/

---

Fourth Lesson: Permissions

Three permission levels:
- allow: runs immediately
- ask: pauses for approval (Allow Once / Allow Always / Reject)
- deny: blocked entirely

Added Git guardrails to the bash block:
- git push *: ask — confirm before pushing to remote
- git checkout *: ask — confirm before switching branches (prevents losing uncommitted work)

Also learned about external_directory (controls access outside the project) and per-project permissions (.opencode/opencode.json in a project overrides global rules for that project).

https://opencode.school/lessons/permissions/

---

Fifth Lesson: Instructions

Created ~/.config/opencode/AGENTS.md — OpenCode reads this file at the start of every session and follows whatever I write there.

Key differences from opencode.jsonc instructions:
- Config instructions = URLs (OpenCode fetches content from a server)
- AGENTS.md = local file on my machine (I write and control it directly)

Two types:
- Global (~/.config/opencode/AGENTS.md) — personal, not shared
- Project (AGENTS.md in project root) — committed to Git, shared with team

My AGENTS.md includes: my name, student ID, OS, coding level, communication preferences, teaching style preferences.

https://opencode.school/lessons/instructions/

---

Sixth Lesson: Models

Cost vs capability tradeoff:
- Paid models (Claude, GPT-5) — most capable, cost money per request
- OpenCode Go ($10/mo) — solid mid-tier, some have vision
- OpenCode Zen (free) — good for learning, most lack vision

Change models: click model name below text input or type /model.

Context windows: how much text a model can see at once (in tokens). Big models have 128K-1M tokens, small ones 8K-32K. Different languages use different token counts — the tokenizer is mechanical, not based on meaning.

Cloudflare AI Gateway: routes requests to multiple AI providers through one Cloudflare bill instead of separate API keys.

https://opencode.school/lessons/models/

---

Seventh Lesson: Commands (in progress)

Custom commands = reusable slash prompts saved as files or JSON.

Two ways to create them:
- Markdown file in ~/.config/opencode/commands/ (filename = command name)
- JSON entry in opencode.jsonc under "command" key

$ARGUMENTS = a fill-in-the-blank placeholder. Example:
  Command file says: "Explain what $ARGUMENTS does in plain language."
  /explain git push → model sees: "Explain what git push does in plain language."
  /explain tokens  → model sees: "Explain what tokens does in plain language."

Created ~/.config/opencode/commands/explain.md as an example of the $ARGUMENTS pattern.

Frontmatter options (optional):
- model: pins a command to a specific AI model
- agent: pins a command to a specific agent (plan/build)
- description: shown in the command list

Created ~/.config/opencode/commands/summarize.md for the verification step.

https://opencode.school/lessons/commands/

---

Eighth Lesson: Skills

Skills = reusable instruction packs (SKILL.md files) that teach OpenCode how to do specific tasks it wouldn't otherwise know.

Originally created by Anthropic, now an open standard at agentskills.io, supported by 40+ AI tools.

Skills live in folders under ~/.agents/skills/ or ~/.config/opencode/skills/. At minimum a SKILL.md with name, description, and instructions. Can also bundle scripts, reference docs, and assets.

Agents use skills two ways:
- Automatically: when a task matches the skill's description
- Manually: user asks for the skill by name

Installed 7 Replicate skills via: npx skills add replicate/skills --yes --global
Skills installed: build-models, compare-models, find-models, prompt-images, prompt-videos, publish-models, run-models

Example project skill: created .opencode/skills/chirpy-upgrade/SKILL.md for this blog. It contains the full upgrade workflow (adding upstream, fetching tags, merging, resolving submodule conflicts, npm run build). OpenCode loads it automatically when I mention upgrading the blog.

https://opencode.school/lessons/skills/

---

Ninth Lesson: Tools

Tools = functions the AI can call to do things beyond generating text (edit files, run commands, fetch data). This is what makes OpenCode an agent, not just a chatbot.

MCP (Model Context Protocol) = open standard for connecting AI to external tools.
- Local servers: run on your machine via npx
- Remote servers: run in the cloud, connected by URL

Three auth levels:
- Public: no credentials needed
- API key: stored in environment variable
- OAuth: opens browser to log in

Added weather MCP server (open-meteo) to opencode.jsonc.
Added MCP authentication section to AGENTS.md.

Key difference from skills: skills are recipe books (instructions), MCP servers are working kitchens (actual running programs that do things).

https://opencode.school/lessons/tools/

---

Tenth Lesson: Plugins

Plugins = JS/TS modules that extend OpenCode beyond what MCP can do. They can hook into lifecycle events, add custom tools, modify how existing tools behave, and ship companion skills.

Layman's comparison:
- Skill = advice (a recipe)
- MCP server = appliance (a single-purpose program)
- Plugin = remodeling (changes behavior, adds custom tools, hooks into events)

Two scopes:
- Project: .opencode/plugins/
- Global: ~/.config/opencode/plugins/

Installed Replicate plugin (4 tools: replicate_search, replicate_run, replicate_schema, replicate_whoami) + companion skill. Requires REPLICATE_API_TOKEN in .bashrc.

https://opencode.school/lessons/plugins/

---

Eleventh Lesson: Agents

Two built-in agents:
- Plan: read-only, conversational. Read files, discuss, research. Won't edit or run destructive commands. Set as default in Configuration lesson. Important: it's a strong guardrail, not a hard sandbox — occasional API calls or side effects may still happen.
- Build: full read/write/run access. Switch when ready to implement.

Switch between them: press Tab (terminal) or dropdown (desktop).

Recommended workflow: Start in Plan → explore → switch to Build → implement. For quick simple tasks, go straight to Build.

My take: use Plan for complex/destructive changes, Build for simple stuff or when ready to execute.

https://opencode.school/lessons/agents/

---

Twelfth Lesson: Sessions

A session = one conversation thread with its own history. Start new ones with /new or sidebar button. Old sessions persist on disk — resume any time.

Sharing:
- /share — generates public link at opncd.ai/s/<id>
- /unshare — removes it
- Three modes: manual (default), auto (share every session), disabled (never share)

CLI commands: opencode session list, opencode export <sessionID>

Ran session export on my Interview lesson session — deepseek-v4-pro, ~$0.30 cost, 555K input tokens.

https://opencode.school/lessons/sessions/

---

Thirteenth Lesson: Images

Vision models can interpret images: describe photos, extract text from screenshots, analyze UI layout/colors/spacing.

Add images: drag-and-drop (desktop) or provide file path (terminal).

Vision support: Claude (all), GPT-4/5, Gemini 3, Kimi K2.5. Free Zen models (Big Pickle, MiMo, Nemotron, MiniMax) not confirmed. DeepSeek v4 Pro does NOT support vision.

Verified: tried pasting screenshot, deepseek-v4-pro responded "this model does not support image input." Practical uses: recreate UI designs, debug visual bugs, implement mockups, extract text from images.

https://opencode.school/lessons/images/

---

Fourteenth Lesson: Workspaces (FINAL)

Workspaces = isolated copies of project files on their own Git branch. Prevents multiple sessions from overwriting each other's changes.

Desktop-only feature (requires right-click in sidebar). Under the hood: uses Git worktrees, creates branch named opencode/<name> in separate directory.

NOTE: I use the terminal (TUI), so I can't use workspaces — they're Desktop-only. Took the quiz and completed the lesson conceptually.

https://opencode.school/lessons/workspaces/

---

ALL 14 LESSONS COMPLETE

---

# Bonus: Commands vs Skills (Layman's Terms)

Both give instructions to the AI. The difference is **how they trigger** and **what they're for**.

## Commands = a button you press

You type `/something`. It runs. You're in control.

Use when: you want a shortcut, you know exactly when you want it, the task is simple.

Examples:
- `/start` → opens file explorer
- `/summarize` → summarizes the project
- `/explain git push` → explains something in layman's terms

## Skills = an automatic sensor

You talk normally. The AI detects what you need and loads the skill on its own. No slash needed.

Use when: the task is complex (multi-step), you want the AI to "just know" it, you might forget the exact procedure.

Examples:
- Chirpy upgrade skill → triggers when you say "upgrade my blog"
- Replicate skills → trigger when you mention AI models/images

## Quick rule of thumb

| Question | Answer |
|----------|--------|
| "Do I want to push a button?" | → Command |
| "Should the AI figure it out on its own?" | → Skill |
| Simple one-shot task? | → Command |
| Multi-step workflow with edge cases? | → Skill |
| I want to control exactly when it fires? | → Command |
| I want it to work in Claude Code, Codex, AND OpenCode? | → Skill |

## Analogy

A command is a **light switch** — you flip it on purpose.

A skill is a **motion sensor** — it triggers when you walk into the room.
