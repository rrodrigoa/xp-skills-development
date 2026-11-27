# Decorator

## Use when
Add independently composable behavior around the same interface.

## Avoid when
One permanent behavior belongs directly in implementation.

## Implementation
Wrap same interface and delegate; preserve results/errors; define ordering and ownership. Function wrappers may suffice for callable contracts.

## Verification and review
Test composition order, delegation, errors and unchanged contract.

## Refactoring recipe
**Trigger:** Logging, retry or metrics logic is copied across interchangeable providers.

**Migration:** Extract common contract; wrap one cross-cutting concern at a time; compose wrappers at boundary, preserve invocation/result semantics and document ordering.

**Acceptance:** Test wrapper alone and combinations, error propagation, exactly-once invocation where required.

**Tradeoff:** Use a simple function decorator for stateless behavior; retry can change side effects and requires idempotency analysis.
