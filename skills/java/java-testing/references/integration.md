# Java integration and Testcontainers

## Shared guidance
dev-testing: integration, e2e, contract

## When to load
Test database, broker, HTTP or deployment behavior.

## Language-specific decisions
Use approved real dependency fixture or Testcontainers, pin service images and isolate schema/data. Establish bounded readiness and teardown. For Spring, use focused slices when possible and full context for integration behavior; verify transactional boundaries with real commits.

## Verification and evidence
Record container versions, test counts, cleanup, error paths and startup/connection failures.

## Avoid
In-memory substitute claimed as production database compatibility or rollback masking commit bugs.
