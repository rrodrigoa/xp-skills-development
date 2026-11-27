# Java enterprise and distributed patterns

## Shared guidance
oo-patterns: repository, unit-of-work, specification, registry, object-pool, outbox, cqrs, state-machine, pipeline, saga, circuit-breaker, null-object

## When to load
Design persistence, state transitions or distributed workflow.

## Language-specific decisions
Use repository ports with explicit transaction scope; if using JPA, separate persistence lifecycle from business invariants where practical. Use Predicate for simple specifications; typed registry or ServiceLoader for extensions. Prefer approved connection pools and resilience libraries. Persist outbox with state and design duplicate handling; sagas require explicit compensation rather than assumed rollback.

## Verification and evidence
Contract-test adapters, transaction rollback, optimistic concurrency, replay, pool exhaustion and failure recovery.

## Avoid
Exposing ORM session to domain callers or treating CQRS as mandatory separate databases.
