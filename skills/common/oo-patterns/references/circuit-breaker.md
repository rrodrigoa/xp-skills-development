# Circuit Breaker

## Use when
Repeated remote failures waste capacity.

## Avoid when
Local operation or no meaningful recovery mechanism.

## Implementation
Use closed/open/half-open state and bounded probes with monotonic clock; separate timeout and retry policies.

## Verification and review
Test state transitions and concurrent probe limits.

## Refactoring recipe
**Trigger:** Repeated downstream failures overwhelm caller or dependency.

**Migration:** Measure failure modes; define closed/open/half-open transitions and scope, wrap downstream call, distinguish timeout/retry and fallback policies.

**Acceptance:** Test threshold, cooldown, concurrent probes, recovery and observable open state.

**Tradeoff:** Avoid masking errors or applying breaker to local validation; use existing library if appropriate.
