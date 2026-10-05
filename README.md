# NEXUS
Autonomous Personal Intelligence System

NEXUS is a modular personal AI operating layer for Windows desktop use. This repository contains a working foundation for:

- a backend AI orchestrator
- a task planner and memory store
- a provider abstraction for local/cloud models
- a permission and approval engine
- a telemetry-aware system dashboard
- a browser-served desktop shell UI
- basic voice and tool abstractions

## Quick start

1. Create a virtual environment
2. Install dependencies
3. Copy `.env.example` to `.env`
4. Start the app

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
python -m nexus.main
```

Then open:

- http://localhost:8000

## Included features

- Real system telemetry from `psutil`
- Event bus and tool registry
- Memory store with search/update/delete
- Permission engine with approval checks
- Task planner for goals and subtasks
- Local provider fallback for offline operation
- UI dashboard and chat shell
- API endpoints for chat, tasks, memory, and system status

## Safety

NEXUS does not auto-execute unrestricted destructive system commands. High-risk actions require explicit approval, and the architecture is designed to keep tool execution behind permissions and validation.

## Documentation

- SETUP.md
- ARCHITECTURE.md
- SECURITY.md
- DEVELOPMENT.md
- TROUBLESHOOTING.md
