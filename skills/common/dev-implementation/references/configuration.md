# Configuration and settings

## Use when
Settings vary by environment or invocation.

## Avoid when
Reading environment throughout business code.

## Implementation
Parse once at bootstrap into typed settings; document precedence; inject narrow config; separate secrets, fail fast on missing required settings.

## Verification and review
Test precedence, invalid values, and redacted repr/log output.
