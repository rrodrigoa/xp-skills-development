# Object Pool

## Use when
Expensive limited reusable resources need bounded checkout.

## Avoid when
Cheap objects or existing library pool.

## Implementation
Use supported pool when possible; bound size, validate resources, use context-managed borrow and return.

## Verification and review
Test timeout, broken resource disposal and concurrent use.

## Refactoring recipe
**Trigger:** Repeated expensive resource creation or exhaustion is measured.

**Migration:** Define capacity, checkout timeout, reset and discard semantics; introduce scoped pool around existing creation, migrate consumers to guaranteed return.

**Acceptance:** Test saturation, cancellation, failed resources, shutdown and leakage.

**Tradeoff:** Prefer provider-native pool; no unbounded allocation or reuse of contaminated resources.
