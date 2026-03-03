# OpenClaw Mission Control

Multi-workspace dashboard for Ranni, Company (router), and Melina agents.

## Structure

```
data/
  ranni/          # Ranni personal workspace
  company/        # Company/router workspace
  melina/         # Melina capital workspace
    tasks.json    # Kanban task board
    projects.json # Project tracking
    cron.json     # Cron jobs (calendar)
    agent.json    # Agent status & activity feed
```

## How it works

Each agent writes to its own `data/{workspace}/` directory and pushes via git.
The dashboard reads the JSON files and renders the UI.
Calendar view merges all three `cron.json` files with workspace filtering.

## Access

GitHub Pages: https://scatterai01.github.io/openclaw-mission-control/
