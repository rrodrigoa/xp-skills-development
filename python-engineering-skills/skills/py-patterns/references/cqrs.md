# CQRS

## Use when
Read and write models have genuinely different needs.

## Avoid when
Ordinary CRUD or premature microservices.

## Implementation
Separate commands from query model; define consistency and projection lag; start within one process if possible.

## Verification and review
Test projection rebuild, lag and write invariants.

## Refactoring recipe
**Trigger:** Read and write requirements diverge and one model compromises both.

**Migration:** Separate command invariants from read projection, define freshness and consistency, migrate selected queries, introduce projection rebuild and reconciliation.

**Acceptance:** Test stale reads, eventual update, replay and authorization on both paths.

**Tradeoff:** Do not require separate database or event sourcing when simple read/write methods suffice.
