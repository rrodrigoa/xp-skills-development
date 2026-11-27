# Explicit state machine

## Use when
Workflow requires auditable transitions.

## Avoid when
Simple one-shot function.

## Implementation
Model states/events and allowed transitions, persist version, guard concurrency and terminal states.

## Verification and review
Test transition matrix and replay.

## Refactoring recipe
**Trigger:** Workflow transitions are implicit in flags and scattered conditionals.

**Migration:** Inventory states, events, guards and side effects; define allowed transition table, route old entry points through state owner, persist compatible transitions.

**Acceptance:** Test all transitions, rejected events, concurrent updates and recovery.

**Tradeoff:** Do not confuse state machine with state pattern; simple table often sufficient.
