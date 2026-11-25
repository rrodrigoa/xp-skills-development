# Timeouts, retry and circuit breaker

## Use when
Remote operations have transient faults.

## Avoid when
Retry non-idempotent mutations blindly or infinite retries.

## Implementation
Set per-call and overall deadlines; classify retryable errors; bounded exponential backoff with jitter; respect Retry-After; use idempotency keys or reconciliation.

## Verification and review
Test permanent errors, exhaustion, cancellation and duplicate side effects.
