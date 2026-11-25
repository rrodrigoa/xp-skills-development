# Application service and use cases

## Use when
Multiple entry points need the same business operation.

## Avoid when
Thin wrappers forwarding every call without policy or orchestration.

## Implementation
Use service object for shared dependencies and use-case methods; keep domain decisions in domain objects and transaction boundaries at use-case level.

## Verification and review
Call same use case from CLI and tests without CLI imports.
