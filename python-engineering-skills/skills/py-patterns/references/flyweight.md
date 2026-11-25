# Flyweight

## Use when
Many objects repeat immutable intrinsic state causing measured memory cost.

## Avoid when
No measured issue or shared state is mutable.

## Implementation
Intern immutable intrinsic state with bounded or weak cache; store extrinsic state on each caller.

## Verification and review
Test shared identity, independent extrinsic state and cache bounds.

## Refactoring recipe
**Trigger:** Memory profile shows repeated immutable data across many objects.

**Migration:** Measure actual duplication; separate intrinsic immutable state from per-instance extrinsic state; scope interning/cache and migrate constructors.

**Acceptance:** Measure memory and latency, ensure independent mutable state and bounded cache.

**Tradeoff:** Do not intern mutable user data or use unbounded caches without evidence.
