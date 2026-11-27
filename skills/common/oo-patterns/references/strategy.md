# Strategy

## Use when
Algorithm varies independently of its caller.

## Avoid when
One simple stable algorithm.

## Implementation
Use a callable or narrow interface with concrete strategies; inject selection at boundary; keep caller independent of implementation.

## Verification and review
Run common behavioral tests for strategies and add one without modifying caller.

## Refactoring recipe
**Trigger:** Algorithm varies across call sites and conditionals are repeatedly edited.

**Migration:** Characterize variants, extract narrow callable/protocol, wrap old algorithm as default, inject selection at boundary, migrate one caller at a time.

**Acceptance:** Shared behavior tests, variant-specific edge cases, unknown selection and extension without caller edits.

**Tradeoff:** Use direct function or dictionary dispatch for trivial stateless alternatives.
