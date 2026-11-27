# Property-based and fuzz tests

## Use when
Large input space, parsing, invariants or roundtrips.

## Avoid when
Properties that simply repeat implementation.

## Implementation
Use a property-based testing framework where approved; define independent invariant or oracle, generate boundary cases, retain shrunk reproductions.

## Verification and review
Test roundtrip, idempotence, monotonicity or conservation as applicable.
