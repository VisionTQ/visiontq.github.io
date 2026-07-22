---
title: How I Made a Terminal Shortcut for My Blog Server
date: 2026-07-22
description: From typing three commands to typing one word. How aliases work and how I set one up for my Jekyll blog.
tags:
  - terminal
  - blog
  - jekyll
categories:
  - chirpy
image:
  path: /assets/img/terminal-alias-blog-server.jpg
  alt: Terminal window with the nb alias command
---

Every time I wanted to preview my blog locally, I had to do three things:

1. Open the terminal
2. Type `cd ~/Desktop/Nebula0/nebula0.com` (navigate to the blog folder)
3. Type `bundle exec jekyll serve` (start the server)

Now I just type `nb`.

## What `~/.bashrc` Is

`~/.bashrc` is a hidden text file in your home folder. Breaking the name down:

- `~` = your home folder (in my case, `/home/tariq`)
- `.` at the start of `bashrc` = a hidden file (press `Ctrl+H` in your file manager to see hidden files)
- `bashrc` = "bash run commands": a config file the terminal reads every time you open it

You can view this file with any text editor. 

Because the terminal reads this file on startup, anything you put in it runs automatically every time you open a new terminal window.

## Typing an Alias vs Saving One

You can define an alias two ways:

| Method | How long it lasts |
|--------|-------------------|
| Type it directly in the terminal | Disappears when you close the window |
| Save it to `~/.bashrc` | Stays forever |

If I had just typed `alias nb='...'` in the terminal, the shortcut would only work in that one window and would be gone after I closed it. By adding the line to `~/.bashrc`, it's saved permanently.

## What OpenCode Added

I opened `~/.bashrc` and added this line to the bottom:

```bash
alias nb='cd ~/Desktop/Nebula0/nebula0.com && bundle exec jekyll serve'
```

Breaking it down:

- `alias nb=` — creates a shortcut called `nb` (short for nebula)
- `cd ~/Desktop/Nebula0/nebula0.com` — step 2 from above: navigate to the blog folder
- `&&` — "if the first part worked, run the next." Chains commands together
- `bundle exec jekyll serve` — step 3: start the local server

## Making It Work

Since I already had a terminal open when the file was edited, I ran `source ~/.bashrc` once. This tells the terminal: "re-read the file now" instead of waiting for me to open a new terminal.

If you open a brand new terminal, the alias is already there & no need to run anything.

## Usage

From now on, I open the terminal, type `nb`, and the server starts. `Ctrl+C` stops it. Best time saver ever lol.
