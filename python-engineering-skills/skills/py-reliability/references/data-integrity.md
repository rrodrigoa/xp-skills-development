# Transactions, idempotency and atomic writes

## Use when
Durable state and retried mutations.

## Avoid when
Assuming exactly-once delivery or using read-then-write without protection.

## Implementation
Use transaction, uniqueness constraints/version checks; idempotency keys with scoped payload identity; outbox for atomic publish intent; reconcile ambiguous outcomes.

## Verification and review
Test duplicate deliveries, crash windows, concurrency and rollback.
