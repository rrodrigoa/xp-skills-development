# Repository

## Use when
Domain needs collection-like persistence.

## Avoid when
Generic CRUD wrapping ORM without domain benefit.

## Implementation
Define consumer-owned port with domain-specific methods; map database records in adapter.

## Verification and review
Shared contract with real and fake adapters.

## Refactoring recipe
**Trigger:** Persistence queries and mapping leak into business rules.

**Migration:** Define domain-oriented operations and transaction scope, wrap existing storage, migrate service calls and remove ORM types from core boundary.

**Acceptance:** Shared adapter contract, missing records, concurrency and transaction behavior.

**Tradeoff:** Avoid generic CRUD wrapper if application needs no persistence abstraction.
