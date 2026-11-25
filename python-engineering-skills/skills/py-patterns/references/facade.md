# Facade

## Use when
Consumers need a simple entry point to a complex subsystem.

## Avoid when
Pass-through wrapper with no simplification.

## Implementation
Expose cohesive high-level operations, orchestrate collaborators, keep escape hatches explicit if needed.

## Verification and review
Test public workflow and failure handling without private calls.

## Refactoring recipe
**Trigger:** Consumers repeatedly coordinate multiple internal components to perform same use case.

**Migration:** Identify stable consumer operation, extract facade delegating to owners; migrate one consumer at a time and keep internals accessible only where appropriate.

**Acceptance:** Test equivalent output, error and ordering; ensure policy stays with responsible domain/service.

**Tradeoff:** Avoid a god facade or empty wrapper around single function.
