# Exceptions and error contracts

## Use when
Operations can fail or cross a boundary.

## Avoid when
Catching Exception and returning None or success.

## Implementation
Define meaningful exception types when callers distinguish failures; preserve causes with raise ... from exc; translate at adapters; avoid secrets in messages. Finally/context manager handles cleanup.

## Verification and review
Test error type, message where contract, causal chain and cleanup.
