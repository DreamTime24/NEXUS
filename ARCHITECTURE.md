# Architecture

## Design decisions

This is a modular but intentionally lightweight implementation. It avoids a fake monolithic app and instead keeps responsibility separated into a small set of focused modules.

## Core modules

- `nexus.config` - environment configuration
- `nexus.event_bus` - internal event system
- `nexus.providers` - AI provider abstraction
- `nexus.tools` - tool registry and execution wrappers
- `nexus.security` - permission and approval logic
- `nexus.memory` - in-memory persistence and memory APIs
- `nexus.tasks` - hierarchical goal/task planning
- `nexus.telemetry` - system usage metrics
- `nexus.voice` - local voice placeholders and abstractions
- `nexus.api` - FastAPI routes for the app
- `nexus.frontend` - static dashboard and chat interface

## Execution flow

The orchestrator follows the secure loop:

```text
input -> intent -> plan -> permission check -> tool execution -> verification -> response
```

No raw model-generated shell commands are executed directly. Tool execution goes through validation, permissions, and risk classification.

## Desktop shell strategy

The repository uses a web-based desktop shell served by the backend. This is a practical, maintainable approach for a local desktop experience without requiring a heavy Electron or Tauri build in the initial implementation.

## Future expansion paths

- add real Ollama/OpenAI integrations
- add SQLite/Postgres persistence
- add browser automation tools
- add true Windows accessibility automation
- add screenshot/OCR modules
- add Tauri/Electron packaging later
