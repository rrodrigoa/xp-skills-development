# Resource lifecycle and deterministic cleanup

## Use when
File, socket, session, lock or transaction ownership.

## Avoid when
Relying on finalization or process exit.

## Implementation
Use deterministic resource scopes and reverse-order cleanup; distinguish borrowed vs owned resources; make close idempotent if contract requires; release after partial initialization.

## Verification and review
Inject exceptions and verify close/release, including cancellation.
