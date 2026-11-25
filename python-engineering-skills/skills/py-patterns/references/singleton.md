# Singleton

## Use when
Exactly one resource per explicit scope is required.

## Avoid when
Global service locator or convenient shared mutable state.

## Implementation
Prefer one instance wired by composition root; module-level immutable constants are fine; process singleton is not distributed singleton. Define scope and lifecycle.

## Verification and review
Test identity within scope and isolation between test scopes.

## Refactoring recipe
**Trigger:** Global resource creation accidentally produces multiple competing instances.

**Migration:** Define actual scope (process, application, request) and lifecycle; move construction to composition root, inject same instance to consumers, remove global lookups incrementally.

**Acceptance:** Test separate application instances, shutdown, concurrency and test isolation.

**Tradeoff:** Prefer dependency injection and scoped lifetime; do not introduce global mutable singleton to avoid passing dependencies.
