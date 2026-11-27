# Chain of Responsibility

## Use when
Multiple handlers may handle or pass a request.

## Avoid when
Single fixed conditional or all steps always execute.

## Implementation
Define handled/unhandled result explicitly; order handlers; terminate with defined default; distinguish middleware pipeline.

## Verification and review
Test first match, ordering, unhandled and exception path.

## Refactoring recipe
**Trigger:** Long conditional sequence selects a handler or passes request along.

**Migration:** Characterize order, first-match versus multi-handler and default; define handler result semantics, extract existing branches and compose explicit order.

**Acceptance:** Test overlap, no match, short circuit, errors and registration order.

**Tradeoff:** Use direct dispatch table if matching is unique and simple.
