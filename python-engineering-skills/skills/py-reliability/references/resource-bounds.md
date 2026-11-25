# Resource limits and backpressure

## Use when
Potentially large input, queue or output.

## Avoid when
Unlimited memory, concurrency or recursive parsing.

## Implementation
Set size/depth/concurrency limits, streaming where useful, bounded queues, admission policy and cancellation; surface actionable overload errors.

## Verification and review
Load and adversarial tests verify predictable bounds.
