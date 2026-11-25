# Resource lifecycle and context managers

## Use when
File, socket, session, lock or transaction ownership.

## Avoid when
Relying on __del__ or process exit.

## Implementation
Use context managers/ExitStack; distinguish borrowed vs owned resources; make close idempotent if contract requires; release after partial initialization.

## Verification and review
Inject exceptions and verify close/release, including cancellation.
