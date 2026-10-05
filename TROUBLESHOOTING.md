# Troubleshooting

## Port already in use

Change the port in `.env` or run the app with a different host/port argument.

## Import errors

Reinstall dependencies:

```bash
pip install -r requirements.txt
```

## Missing telemetry

On some systems, some metrics may be unavailable. The app reports those as `Unavailable` instead of inventing values.

## Safety blocks

If a tool request is denied, check the permission and approval settings in the configuration or tool registry.
