# Caching and invalidation

## Use when
Repeated expensive deterministic or versioned queries.

## Avoid when
Caching mutable data without scope, invalidation or bounds.

## Implementation
Define key with relevant version/tenant/config; bound size/TTL, avoid stale permissions, handle concurrency and stampedes, expose hit/miss and invalidation.

## Verification and review
Test eviction, expiry, key isolation, concurrent calls and changed source.
