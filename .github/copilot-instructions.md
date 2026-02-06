# Copilot Instructions

## Project Overview

This is a **GitHub Copilot CLI workshop** — a hands-on guide teaching developers how to use the Copilot CLI through 12 sequential modules covering installation, sessions, tools, MCP servers, skills, custom agents, hooks, and advanced topics.

## Repository Structure

- `docs/workshop/` — Workshop modules numbered `00-12`, designed to be followed in order
- `tryout/` — Scratch directory for workshop exercises (Docker-mounted workspace)
- `FEEDBACK.md` — Tracks workshop issues; resolved items have inline `⚠️ **FEEDBACK**` notes in modules

## Workshop Flow

```
Installation (01) → Core Concepts (02-05) → Advanced (06-12)
```

**Total duration**: ~4 hours

## Running the Workshop

The workshop can run directly (Node.js 22+) or in a Docker container:

```bash
# Start isolated container
docker run -it --name copilot-workshop \
  -v "${HOST_PROJECT_PATH:-$(pwd)}/tryout":/workspace \
  -w /workspace ubuntu:24.04 bash

# Inside container: install prerequisites
apt-get update && apt-get install -y curl git jq gh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
source ~/.bashrc && nvm install --lts
```

## Key Conventions

- **Module structure**: Each module follows Goal → Steps → Expected Outcome format
- **Feedback markers**: Version-specific or unverified features use `⚠️ **FEEDBACK**` callouts
- **Docker container**: Named `copilot-workshop` with `tryout/` mounted at `/workspace`

## When Editing Workshop Modules

- Maintain the existing exercise structure (Goal, Steps, Expected Outcome)
- Add `⚠️ **FEEDBACK**` callouts for version-specific features or known issues
- Update `FEEDBACK.md` when resolving or discovering issues
