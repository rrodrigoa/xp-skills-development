# Java AutoCloseable and lifecycle

## Shared guidance
dev-implementation: resource-lifecycle; dev-reliability: resource-bounds

## When to load
Own streams, sockets, JDBC connections or executors.

## Language-specific decisions
Use try-with-resources for AutoCloseable scopes and explicit ownership. Close dependent resources in reverse order, preserve suppressed cleanup failures and define application shutdown. Check JDK-specific executor lifecycle APIs; use explicit shutdown/await where required.

## Verification and evidence
Inject acquisition and operation failures; inspect suppressed causes, pool reuse and termination.

## Avoid
Finalizers/GC for deterministic cleanup or closing resources borrowed from caller.
