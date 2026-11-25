# Unit of Work

## Use when
Several writes need one atomic transaction.

## Avoid when
Single independent operation with transaction already managed.

## Implementation
Use context manager, explicit commit, rollback on uncommitted exit, owned session cleanup.

## Verification and review
Test commit, rollback and exceptions.

## Refactoring recipe
**Trigger:** A use case performs multiple writes without explicit atomic ownership.

**Migration:** Identify transaction boundary, introduce scoped transaction owner around old adapters, migrate service to explicit success/rollback and isolate lifecycle.

**Acceptance:** Test mid-operation failure, rollback, commit failure and resource release against real storage.

**Tradeoff:** Do not claim atomicity across independent stores; use compensation or other consistency design.
