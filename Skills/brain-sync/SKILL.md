---
name: brain-sync
description: "Use to sync the Obsidian second brain to GitHub."
version: 1.0.0
author: Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [obsidian, sync, github, memory, backup]
---

# Sync Second Brain (Obsidian + GitHub)

Use this skill whenever the user asks to save, sync, backup, or push the second brain (Obsidian vault). This ensures everything generated during the session is safely backed up to GitHub.

## Location
The second brain is located at `~/HermesBrain`.
It contains:
- `Skills/`: New skills are created here (`config.yaml: skills.create_dir`).
- `Dados/`: For general files, spreadsheets, text data, etc.
- `Memorias/`: For markdown logs or summaries.

## Workflow

To sync the brain to GitHub, run this snippet via terminal:

```bash
cd ~/HermesBrain
git add .
git commit -m "Auto-sync by Hermes: $(date +'%Y-%m-%d %H:%M')" || true
git push
```

If `git push` fails due to authentication, inform the user they need to authenticate Git (e.g. `gh auth login`).

## After generating new skills or data
If you created a new skill or file during a session, proactively offer to run `brain-sync` at the end of the conversation.
