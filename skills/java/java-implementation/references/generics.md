# Java generics and type erasure

## Shared guidance
dev-implementation: typing; oo-design: solid-lsp

## When to load
Define collections, adapters and generic contracts.

## Language-specific decisions
Prefer parameterized types, narrow bounds, producer extends/consumer super where appropriate, and avoid raw types or unchecked casts. Type erasure limits runtime generic discrimination; use explicit type tokens only when needed. Use primitive-specialized types where measured benefit warrants it.

## Verification and evidence
Compile with approved warnings, inspect unchecked suppression scope and test mixed/invalid input at runtime boundaries.

## Avoid
Overgeneric public APIs or assuming generic types are reified.
