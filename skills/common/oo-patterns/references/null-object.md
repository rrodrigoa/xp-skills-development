# Null Object

## Use when
Optional collaborator has legitimate no-op semantics.

## Avoid when
Failure must be visible or authorization required.

## Implementation
Provide same contract with explicitly documented neutral behavior; select at composition root.

## Verification and review
Verify neutral behavior does not mask errors.

## Refactoring recipe
**Trigger:** Repeated optional collaborator checks represent a legitimate neutral behavior.

**Migration:** Define semantics of no-op, implement neutral collaborator, inject only at optional boundary, remove conditional checks after characterization.

**Acceptance:** Test neutral return, no side effects and explicit behavior when mandatory collaborator is missing.

**Tradeoff:** Never replace required authorization, persistence or error reporting with no-op.
