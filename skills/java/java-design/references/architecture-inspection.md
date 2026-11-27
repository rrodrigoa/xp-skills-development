# Java architecture graph and static-heavy code

## Shared guidance
dev-architecture-analysis: import-graph, procedural-density, coupling, cycles

## When to load
Audit dependencies and OO quality.

## Language-specific decisions
Analyze packages, build modules and compiled classes; imports alone miss fully qualified types and reflection. Use jdeps for compiled static dependency evidence and ArchUnit where approved for rules; account for generated classes, framework wiring, ServiceLoader and runtime dependencies separately. Inspect static mutable state, anemic entities, giant services and feature envy.

## Verification and evidence
Record classpath/module path, artifact revision, scope, edge types, unresolved dependencies and sample provenance; compare against architecture contracts.

## Avoid
Class-count targets or assuming a clean jdeps report proves runtime isolation.
