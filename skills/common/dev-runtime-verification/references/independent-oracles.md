# Runtime assertions and differential oracles

## When to load
Verifying business correctness or migration.

## Implementation in the target project
Derive expected outcomes from approved requirements, reference implementation, invariant or independent calculations. Use metamorphic relations when exact output is hard to know; for differential tests define normalization and allowed intentional differences. Assert observable side effects, error classes and state transitions, not just response codes. Include deliberately incorrect implementation or historical failure as negative control.

## Required evidence and acceptance
Oracle detects known incorrect result and accepts valid boundary cases; expected values and tolerance justified independently.

## Guardrails
Two implementations can share a bug; snapshots require review and cannot substitute for semantic assertions.
