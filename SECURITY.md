# Security

## Security principles

- no unrestricted autonomous execution
- tool permissions are explicit
- high-risk operations require approval
- secrets remain in environment variables
- logs redact sensitive values

## Risk levels

- LOW: read-only or informational operations
- MEDIUM: file creation or project commands
- HIGH: destructive or security-sensitive operations

## Approval model

This project uses a manual approval mode by default. A tool execution can be blocked unless the approval gate allows it.

## Secret handling

Never commit credentials to source control. Use `.env` and secure local storage for secret values.

## File and shell safety

This repo intentionally does not implement arbitrary shell execution without risk classification. The tool registry is the enforcement point.
