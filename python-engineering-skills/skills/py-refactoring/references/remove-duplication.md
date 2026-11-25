# Consolidate duplicate behavior

## Use when
Same semantics and fixes repeated in multiple callers.

## Avoid when
Coincidentally similar code likely to diverge.

## Implementation
Compare contracts and failure paths; extract shared policy/implementation at appropriate boundary; preserve distinct adapter differences.

## Verification and review
Regression tests for all callers and shared contract.
