# Template Method

## Use when
A stable workflow has a few well-defined variation hooks.

## Avoid when
Composition with callables is simpler or workflow itself varies.

## Implementation
Base method owns invariant sequence; subclasses override narrow hooks; prefer strategy composition if subclass contract is fragile.

## Verification and review
Test invariant sequence and alternate hooks; errors preserve cleanup.

## Refactoring recipe
**Trigger:** Several workflows duplicate same ordered steps with limited variation.

**Migration:** Identify invariant sequence and variation hooks, characterize order, extract shared workflow and delegate hooks; use inheritance only if stable contract warrants.

**Acceptance:** Test hook order, failure cleanup and substitution across variants.

**Tradeoff:** Prefer composition of steps if workflows vary independently or hook contracts become complex.
