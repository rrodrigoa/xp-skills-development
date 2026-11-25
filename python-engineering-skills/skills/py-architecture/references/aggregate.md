# DDD aggregates and invariants

## Use when
Multiple entities must change consistently within a transaction.

## Avoid when
Treating entire database graph as one aggregate.

## Implementation
Choose root by consistency boundary; expose invariant-preserving methods; reference other aggregates by identity. Keep transactions narrow.

## Verification and review
Concurrent and invalid operations cannot violate aggregate invariants.
