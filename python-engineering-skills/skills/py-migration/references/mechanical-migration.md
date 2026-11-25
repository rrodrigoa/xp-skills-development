# Safe automated mechanical changes

## When to load
Planning a rename, move, import rewrite or other repetitive migration.

## Procedure
Define exact symbol identity, scope, exclusions, language/version and expected transformation. Prefer syntax-aware tooling (for example a CST for source-preserving edits), not regex for arbitrary Python. Preview affected paths and ambiguous matches; apply in small batches; verify idempotence and compile/import behavior in the target project.

## Required evidence and acceptance
Before/after mapping, dry-run diff, ambiguous sites, test results and rollback checkpoint; second application produces no unexpected changes.

## Guardrails
Do not edit generated/vendor files, strings or dynamic references blindly. Never delete user changes or claim unverified dynamic sites were handled.
