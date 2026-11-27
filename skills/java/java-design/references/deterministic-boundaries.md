# Java enforceable API and architecture boundaries

## When to load
Prevent invalid calls and cross-layer dependencies.

## Implementation in the target project
Use dev-enforcement architecture-fitness and types-and-invariants. Use private/package-private constructors, validated immutable objects, sealed hierarchies when supported, explicit interfaces and module boundaries. Use ArchUnit for class dependency rules and jdeps/build graph for module dependencies; test reflection, service loading and DI wiring separately.

## Required evidence and acceptance
Negative compile/architecture fixtures fail and allowed adapters compile and run; dynamic injection tests validate runtime boundaries.

## Guardrails
Java access control and JPMS are not business authorization; respect supported JDK.
