# Python context managers and cleanup

## Shared guidance
dev-implementation: resource-lifecycle; dev-reliability: resource-bounds

## When to load
Manage files, sessions, locks and owned clients.

## Language-specific decisions
Use context managers, async context managers or ExitStack for partial initialization and reverse cleanup. Define ownership and borrow scope. __del__ and garbage collection are not deterministic resource management.

## Verification and evidence
Fault-inject acquisition and operation failures, verify close order and no leaked resources.

## Avoid
Keeping client/session lifetime implicit or closing borrowed resources.
