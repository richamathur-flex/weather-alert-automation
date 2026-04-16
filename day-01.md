# Day 01 — Getting Started with n8n
**Date:** April 16, 2026

## What I Did
- Signed up for n8n Cloud (14-day trial, 1000 executions)
- Explored the n8n dashboard interface
- Started building Project 01: Daily Weather Alert to Email

## Key Concepts Learned

### What is n8n?
- n8n = "nodemation" — a visual workflow automation tool
- Open-source (can self-host) or use n8n Cloud (managed)
- Connects apps via nodes, data flows from left to right

### n8n Dashboard Tabs
- **Workflows** — Where all your automation flows live
- **Credentials** — API keys and logins for connected services
- **Executions** — History of every time a workflow ran
- **Variables** — Reusable values across workflows
- **Data Tables** — Built-in data storage

### Core Building Blocks
1. **Trigger Node** — What starts the workflow (schedule, webhook, event)
2. **Action Node** — What the workflow does (send email, call API, update sheet)
3. **Logic Node** — How the workflow decides (IF conditions, Switch, Merge)

## Project 01: Weather Alert to Email

### Workflow Structure
```
Schedule Trigger (8 AM daily)
    → HTTP Request (OpenWeatherMap API)
        → Gmail (send weather summary)
```

### Steps to Build
1. Create new workflow in n8n
2. Add Schedule Trigger node → set to daily at 8:00 AM
3. Add HTTP Request node → GET request to OpenWeatherMap
4. Add Gmail/Email node → format and send weather data
5. Connect all nodes and test

## Notes to Self
- Always test workflows manually before activating them
- Check the output panel of each node to see what data it passes
- Credentials are stored separately and reused across workflows
