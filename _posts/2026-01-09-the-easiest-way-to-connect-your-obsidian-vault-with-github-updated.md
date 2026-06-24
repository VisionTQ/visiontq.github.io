---
title: "The Easiest Way to Connect Your Obsidian Vault with GitHub (Updated)"
date: 2026-01-09
author: tnebula
description: "Step-by-step guide to connect your Obsidian vault with GitHub for easy blog publishing and note synchronization."
tags: ["obsidian", "github", "git", "blogging", "productivity", "markdown"]
categories: ["Tutorials", "Productivity"]
image: "/assets/obsidian/obsidian-github-cover.png"
---

I use the [Chirpy theme](https://chirpy.cotes.page/posts/getting-started/) with GitHub Pages to publish my blogs, and I wanted a way to publish my blogs easily without leaving Obsidian and opening the command line or Git to type commands. 

By the end of this tutorial, you will be able to sync your notes or publish your blogs from Obsidian to GitHub for free!

## Prerequisites

1. **Create a repository** or use any existing repository on GitHub
2. **[Download Git](https://git-scm.com/downloads)** and install it on your system
3. **Create a personal access token** from GitHub
   - Example: {% include embed/video.html src='/assets/obsidian/personal-access-token-github.mp4' %}
   - Set scopes to "repo" and expiration to "no expiration" or anything you want

## Setup Steps

4. **Install the [Obsidian Git](https://github.com/denolehov/obsidian-git/wiki/Installation)** community plugin
   {% include embed/video.html src='/assets/obsidian/download-obsidian-git.mp4' %}
5. **Create a folder in Obsidian** to store the repository
6. **Run the command** (Cmd/Ctrl + P): `Clone an existing remote repo`
   ![clone-repo-git-plugin.png](/assets/obsidian/clone-repo-git-plugin.png)
7. **Paste the URL** of the repository in the following format:

```bash
https://<PERSONAL_ACCESS_TOKEN>@github.com/<USERNAME>/<REPO>.git
```

For example, it might look like this:

```bash
https://ghp_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX@github.com/USERNAME/REPO-NAME.git
```

8. **Enter the folder name** you created in step 5 (e.g., `remote-blog/`)
   - Leave blank and click enter if it asks for any more options
9. **Restart Obsidian**
10. **Make edits to your notes**
11. **Publish your notes** by running the commands:
    - "Git: commit" 
    - "Git: push"
    - Open the command palette (Cmd/Ctrl + P) to run these commands

## References

- [YouTube Tutorial](https://youtu.be/5YZz38U20ws)
- [Obsidian Forum Guide](https://forum.obsidian.md/t/the-easiest-way-to-setup-obsidian-git-to-backup-notes/51429)
  
  ![Not AI](/assets/img/Written-By-Humans-Not-By-AI-Badge-black.png){: .right }
