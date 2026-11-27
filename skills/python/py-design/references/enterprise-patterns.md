# Python enterprise pattern mapping

## Shared guidance
oo-patterns: repository, unit-of-work, specification, registry, object-pool, outbox, cqrs, state-machine, pipeline, saga, circuit-breaker, null-object

## When to load
Persistence, pipelines, distributed operations or resource reuse.

## Language-specific decisions
Use protocols for repositories and explicit context-managed unit of work; commit is an explicit application decision. Prefer typed callable predicates for specifications. Registries should validate unique names; pooled resources use deterministic borrow/release. Async pipelines and sagas need cancellation and explicit compensation; persist outbox atomically with state.

## Verification and evidence
Contract-test adapters, rollback, duplicate deliveries, failed compensation and recovery.

## Avoid
Treating null object as a way to hide missing configuration or failures.
