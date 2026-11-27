# Exceptions and error contracts

## Use when
Operations can fail or cross a boundary.

## Avoid when
Catching Exception and returning None or success.

## Implementation
Define meaningful exception types when callers distinguish failures; preserve underlying error causes; translate at adapters; avoid secrets in messages. Ensure deterministic cleanup on all paths.

## Verification and review
Test error type, message where contract, causal chain and cleanup.
