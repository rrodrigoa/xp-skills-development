# API and behavior compatibility gate

## When to load
Exports, schemas, CLI, exceptions or supported behaviors change.

## Procedure
Inventory affected contracts and supported consumers. Compare signatures, defaults, outputs, errors, side effects and version compatibility; require regression and consumer tests. Check approved breaking-change decision, deprecation, migration docs and release version.

## Required evidence and acceptance
Contract diff, compatibility test results, version policy and consumer impact.

## Guardrails
A passing type checker does not prove behavior compatibility. Do not approve silently changed public behavior.
