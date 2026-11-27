# Pipeline and middleware

## Use when
Ordered composable stages process a value.

## Avoid when
Unclear order or stages are tightly coupled.

## Implementation
Define typed stage contract, explicit ordering and error/cancellation semantics; avoid global context mutation.

## Verification and review
Test each stage and composition order.

## Refactoring recipe
**Trigger:** Sequential processing is duplicated or deeply nested.

**Migration:** Define typed stages, order, error/cancellation and data ownership; extract existing steps, compose pipeline at boundary and migrate paths.

**Acceptance:** Test individual stages, order, short circuit, partial failure and bounded resources.

**Tradeoff:** Avoid generic middleware if fixed direct calls are clearer.
