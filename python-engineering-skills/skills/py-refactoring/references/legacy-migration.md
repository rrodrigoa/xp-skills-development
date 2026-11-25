# Incremental migration and compatibility

## Use when
Public legacy API needs structural improvement.

## Avoid when
Big-bang replacement without contract or rollout plan.

## Implementation
Introduce new implementation behind facade; migrate callers in slices; deprecate with documented timeline; remove only after approved compatibility policy.

## Verification and review
Test both API paths, installed artifact and rollback plan.
