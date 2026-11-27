# Observer

## Use when
Multiple consumers need notification of changes.

## Avoid when
One direct synchronous dependency.

## Implementation
Expose subscribe/unsubscribe; define synchronous/asynchronous semantics, ordering, error policy and lifetime; avoid hidden global bus.

## Verification and review
Test notification, unsubscribe, reentrancy and failed subscribers.

## Refactoring recipe
**Trigger:** A producer directly calls growing list of independent consumers.

**Migration:** Define event contract, subscribe/unsubscribe lifecycle, ordering and failure handling; migrate consumers, ensure events represent committed state when required.

**Acceptance:** Test no subscribers, multiple subscribers, duplicate delivery, cleanup and reentrancy.

**Tradeoff:** Use direct call for required synchronous collaborator; do not hide critical dependencies in events.
