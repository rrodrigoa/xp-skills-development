# Health, shutdown and recovery

## Use when
Long-lived services or worker processes.

## Avoid when
Health checks that always succeed or abrupt process exit.

## Implementation
Separate readiness/liveness, handle signals, stop accepting work, drain with deadline, release resources; document recovery and dependencies.

## Verification and review
Exercise startup failure, graceful shutdown and partial dependency outage.
