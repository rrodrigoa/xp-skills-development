# Specification

## Use when
Domain predicates need composition and reuse.

## Avoid when
One local predicate.

## Implementation
Compose typed predicates with AND/OR/NOT; distinguish in-memory and database translation.

## Verification and review
Test truth tables and translation equivalence.

## Refactoring recipe
**Trigger:** Same domain predicate is reimplemented across filtering and validation.

**Migration:** Name policy, extract pure predicate or composable specification, define composition and error semantics, migrate callers with same rules.

**Acceptance:** Test boundaries, combinations, equivalence and query translation where used.

**Tradeoff:** Do not hide I/O or side effects in a predicate; avoid abstract expression tree for simple rule.
