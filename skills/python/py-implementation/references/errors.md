# Python exception design

## Shared guidance
dev-implementation: errors

## When to load
Define and translate failures.

## Language-specific decisions
Use specific domain exceptions where callers distinguish outcomes; preserve cause using explicit exception chaining. Catch narrow expected errors, let unexpected failures surface. Ensure cleanup in finally or context manager; preserve cancellation rather than converting to success.

## Verification and evidence
Test exception type, cause, boundary mapping, cleanup and secret redaction.

## Avoid
Bare except, broad except returning None or swallowing failures.
