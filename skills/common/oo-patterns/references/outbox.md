# Transactional Outbox

## Use when
Database change and message intent must be atomic.

## Avoid when
No durable messaging requirement.

## Implementation
Store event in same transaction, publish via worker, mark progress; consumer deduplicates at-least-once delivery.

## Verification and review
Simulate crash after publish before marking and retry.

## Refactoring recipe
**Trigger:** Database commit and message publication can diverge.

**Migration:** Persist message intent with business update in same transaction; introduce publisher with durable progress, migrate producers, add consumer deduplication.

**Acceptance:** Test crash after commit and after publish, replay, ordering and cleanup.

**Tradeoff:** No exactly-once claim; use transactional outbox only with actual durable messaging need.
