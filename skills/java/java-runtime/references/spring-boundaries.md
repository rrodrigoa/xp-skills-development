# Java framework and transaction boundaries

## Shared guidance
oo-design: layered-hexagonal, repository-uow; dev-reliability: data-integrity

## When to load
Work in existing Spring or Jakarta application.

## Language-specific decisions
Keep controllers and persistence adapters thin; use constructor injection and explicit transaction ownership. Understand proxy-based interception, self-invocation, transaction propagation and rollback policy; do not assume annotations apply outside managed calls. Keep lazy persistence access within declared lifetime; review N+1 behavior and concurrency/version checks.

## Verification and evidence
Test real transaction commit/rollback, self-invocation cases, adapter queries, lazy loading and authorization.

## Avoid
Framework-driven domain model by default, blanket transactional annotation or hidden network I/O inside transaction.
