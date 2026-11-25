# Public API surface and leakage

## When to load
Assessing reusable libraries or cross-module contracts.

## Procedure
Inventory documented exports, entry points, CLI flags, schemas and supported imports; inspect accidental re-exports and internal types exposed to consumers. Compare base and head for removals, signature changes, defaults, exceptions and behavioral changes.

## Required evidence and acceptance
Record affected consumers, compatibility evidence and version/deprecation impact.

## Guardrails
A leading underscore is only a convention; supported contract may extend beyond exported symbols. Dynamic consumers may be unknown.
