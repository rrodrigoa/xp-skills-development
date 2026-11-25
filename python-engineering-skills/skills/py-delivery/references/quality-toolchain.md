# Ruff, type checking and quality gates

## Use when
Standardizing local and CI checks.

## Avoid when
Introducing overlapping tools or mass unrelated formatting.

## Implementation
Use existing lint/format/type checker; sensible baseline Ruff plus mypy or Pyright and pytest. Adopt gradually for legacy; branch coverage threshold is project policy.

## Verification and review
Run format check, lint, type check, tests and build; report exact commands.
