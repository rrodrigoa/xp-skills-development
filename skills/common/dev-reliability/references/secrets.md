# Secrets and sensitive information

## Use when
Credentials, tokens or user data used.

## Avoid when
Hardcoded secrets or logging raw config.

## Implementation
Use approved secret store or environment injection, scope credentials, rotate and revoke, redact logs and exceptions; avoid committing .env.

## Verification and review
Test redaction and missing credential behavior; scan artifacts.
