# Saga and compensation

## Use when
Cross-service long-lived operations cannot use one transaction.

## Avoid when
Local transaction suffices.

## Implementation
Persist progress, define idempotent forward and compensating actions; compensation may fail and require reconciliation.

## Verification and review
Test partial failure, duplicate messages and compensation failure.

## Refactoring recipe
**Trigger:** A cross-service operation lacks recovery after partial completion.

**Migration:** Identify steps, irreversible effects and compensations, persist progress, define retry/idempotency and operator escalation; migrate one workflow.

**Acceptance:** Test failure at each step, compensation failure, restart and duplicate messages.

**Tradeoff:** Compensation is not rollback; do not promise full reversibility or hide irreversible effects.
