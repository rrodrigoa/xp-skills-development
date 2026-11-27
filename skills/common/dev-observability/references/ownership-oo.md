# Object-oriented telemetry ownership and instrumentation boundaries

## When to load
Changing code to support observability without degrading design.

## Procedure
Keep domain objects responsible for business invariants, not monitoring backends. Expose meaningful domain outcomes or events to application orchestration; instrument use-case boundaries, adapters and resource owners. Use composition/decorator/interceptor for reusable boundary timing and outcome classification, narrow observer/telemetry ports when replacement or testing justifies them, and dependency injection at composition root. Keep domain-specific success classification in its actual owner rather than generic wrappers guessing from exceptions. A transport middleware measures transport, not business completion. A resource pool owns its own capacity signal. Reuse provider API and instrument handles instead of one class per metric. Keep pure computations free of side effects unless a justified diagnostic boundary exists.

## Required evidence and acceptance
Inspect dependency direction, callers and owner of each signal; test contract unchanged, one terminal observation, no duplicate auto/manual instrumentation, and no backend dependence in domain tests.

## Guardrails
Do not build static global metric bags, scatter metric name strings or force every method to emit telemetry.
