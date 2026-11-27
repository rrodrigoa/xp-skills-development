# Python enforceable API and architecture boundaries

## When to load
Prevent invalid calls and cross-layer imports.

## Implementation in the target project
Use common dev-enforcement architecture-fitness and types-and-invariants. Inspect supported interpreter and type checker; use meaningful dataclasses, enums, narrow Protocol contracts and validated construction. Use Import Linter or a tested AST/symbol check for forbidden imports and account for runtime imports and plugins. Keep internal module conventions but validate external data and permission at runtime.

## Required evidence and acceptance
Negative type/import fixtures fail with approved tools, public valid usage passes and dynamic boundary tests cover escapes.

## Guardrails
Python underscores and annotations alone are not enforcement.
