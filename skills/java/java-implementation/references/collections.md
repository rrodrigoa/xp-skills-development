# Java collections, streams and mutability

## Shared guidance
oo-design: value-objects; dev-implementation: functions-methods

## When to load
Select collections and transformations.

## Language-specific decisions
Choose collection semantics for ordering, uniqueness, complexity and concurrency. Return immutable snapshots where ownership requires it; unmodifiable views are not snapshots. Keep stream operations stateless and non-interfering; use loops when control flow is clearer. Parallel streams require measured benefit and safe reduction.

## Verification and evidence
Test duplicate keys, order, aliasing, empty input and large input; verify no shared mutations.

## Avoid
Modifying collections during traversal or parallel streams for blocking I/O by default.
