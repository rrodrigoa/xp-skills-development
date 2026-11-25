# Repository and unit of work

## Use when
Domain objects need persistence and atomic changes.

## Avoid when
Generic CRUD abstraction over every ORM model.

## Implementation
Expose domain-specific queries; use UoW to own transaction scope; commit explicitly, roll back uncommitted work, close resources.

## Verification and review
Run shared contracts on in-memory and real adapters; test rollback.
