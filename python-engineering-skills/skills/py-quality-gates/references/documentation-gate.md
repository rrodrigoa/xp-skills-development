# Documentation and contract consistency gate

## When to load
Public behavior, configuration, operations or architecture changes.

## Procedure
Identify documentation affected by the change: public API contracts, CLI usage, environment requirements, architecture decisions, migration instructions, failure modes and security limitations. Compare claims with implemented behavior and verification evidence. Ensure meaningful docstrings explain contracts and invariants, not excuses for unimplemented behavior.

## Required evidence and acceptance
List changed contracts and their documentation locations, verify examples in the target project where applicable, and flag stale or misleading statements.

## Guardrails
Do not require comments on obvious code or block a trivial change for unrelated documentation debt. No claims of verified usage without evidence.
