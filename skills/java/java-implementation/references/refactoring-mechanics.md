# Java syntax-aware refactoring

## Shared guidance
dev-refactoring: characterization, procedural-to-objects; dev-migration: mechanical-migration

## When to load
Move methods, types or package APIs.

## Language-specific decisions
Use IDE/refactoring engine or approved OpenRewrite recipe for semantic symbol moves; inventory imports, reflection, configuration names, serialization names, generated sources and public binary signatures. Separate behavior edits from mechanical moves and retain compatibility adapters only with approved plan.

## Verification and evidence
Compile all modules and representative consumers; run behavior/API and reflection/configuration tests.

## Avoid
Search-and-replace across overloaded methods or assuming compilation covers binary compatibility.
