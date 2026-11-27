# Python static checks and evidence

## Shared guidance
dev-delivery: quality-toolchain; dev-quality-gates: static-quality

## When to load
Interpret formatting, lint and typing checks.

## Language-specific decisions
Use configured Ruff or formatter/linter, mypy/Pyright and pytest. Record target Python version and exclusions; compare newly introduced diagnostics rather than deleting rules.

## Verification and evidence
Provide tool version, exact invocation, revision, output and exit code; report missing required results as UNKNOWN.

## Avoid
Changing ignore rules or suppressing errors to pass a PR.
