# Integration tests

## Use when
Real database, filesystem, queue or HTTP contract matters.

## Avoid when
Assuming mock success proves external behavior.

## Implementation
Use disposable services/temp dirs, real migrations, controlled credentials and readiness checks; mark integration tests; clean resources.

## Verification and review
Exercise timeout, rollback, serialization and failure; report skipped infrastructure.
