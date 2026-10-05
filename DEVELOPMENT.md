# Development

## Install

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Test

```bash
pytest -q
```

## Run

```bash
python -m nexus.main
```

## Structure notes

The application is intentionally segmented so each major subsystem can be extended independently without affecting the rest of the system.
