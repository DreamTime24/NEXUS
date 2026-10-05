# Setup

## Prerequisites

- Python 3.11+
- pip
- optional: Node.js for future frontend expansion
- optional: Ollama or OpenAI-compatible API access

## Environment setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
```

## Model providers

This project supports a provider abstraction with the following modes:

- `local` - built-in offline provider used for safe fallback
- future `openai` and `ollama` integrations can be added behind the same interface

The provider selection is controlled with `AI_PROVIDER` and `AI_MODEL` in `.env`.

## Local model setup

If you want a local LLM integration later, run Ollama and set:

```env
AI_PROVIDER=ollama
OLLAMA_BASE_URL=http://localhost:11434
AI_MODEL=llama3.1
```

## Cloud setup

```env
AI_PROVIDER=openai
OPENAI_API_KEY=your_key_here
AI_MODEL=gpt-4o-mini
```

## Running the app

```bash
python -m nexus.main
```

The web UI is served locally at:

- http://localhost:8000

## Windows notes

The project is designed for a Windows desktop environment, but it runs fine as a local app shell on Linux/macOS for development.
