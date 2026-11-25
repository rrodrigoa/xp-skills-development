# Command

## Use when
Actions must be represented as values for queueing, history or execution policy.

## Avoid when
A direct call with no lifecycle or deferred needs.

## Implementation
Represent immutable intent; bind receiver separately or encapsulate execution; define retry/idempotency and undo only when meaningful.

## Verification and review
Test execution, replay behavior and rejected input.

## Refactoring recipe
**Trigger:** Operations are represented by scattered function names and arguments in queues or history.

**Migration:** Define typed operation data and executor contract, wrap existing actions, make dispatch explicit, define authorization, idempotency and undo semantics where valid.

**Acceptance:** Test serialization, unknown operations, failed execution, retries and unauthorized requests.

**Tradeoff:** Do not add generic command bus for direct synchronous calls with no lifecycle need.
