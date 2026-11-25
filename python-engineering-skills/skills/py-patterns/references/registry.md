# Registry

## Use when
Known plugins or strategies are selected by name.

## Avoid when
One static implementation.

## Implementation
Explicitly register typed factories; reject duplicates and unknown keys; freeze after bootstrap if useful.

## Verification and review
Test lookup, duplicate, missing and isolation.

## Refactoring recipe
**Trigger:** Multiple modules maintain competing name-to-provider mappings.

**Migration:** Define name, capabilities, collision and lifecycle semantics; consolidate explicit registration at composition root and migrate lookups.

**Acceptance:** Test duplicates, unknown names, incompatible providers and deterministic registration.

**Tradeoff:** No ambient service locator or arbitrary imports from untrusted input.
