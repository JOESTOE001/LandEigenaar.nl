---
name: start-dev-server
description: Start the local dev servers for LandEigenaar.nl. Use when the user types "start dev server". Runs the frontend (npm run dev) and the backend (uv run ...) in the background.
---

# Start dev server

Run these from the repository root, `/home/user/LandEigenaar.nl`. Start each one in the background so the session stays usable.

## 1. Frontend (Astro)

```bash
cd /home/user/LandEigenaar.nl && npm run dev -- --host 0.0.0.0
```

- Dependencies must exist. If `node_modules` is missing, run `npm ci` first.
- Expected URL: http://localhost:4321/. Report the port with `report_preview_port` (name `web`).
- Log the output to a file so it can be read back.

## 2. Backend (uv)

Not configured yet. The repo currently has no Python project (no `pyproject.toml`).
Once the backend command is known, replace this step with the real command, for example:

```bash
cd <backend-dir> && uv run <command>
```

Until then, skip this step and tell the user the backend was not started.

## Reporting

After starting, tell the user which servers are running, their URLs and log file locations. If a server fails to start, show the last lines of its log.
