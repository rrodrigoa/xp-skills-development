# Architecture makes correct behavior the default

## When to load
New APIs, modules or recurring invalid states.

## Implementation in the target project
Use narrow types, constructors and state transitions to enforce invariants; make dangerous operations unavailable through normal public interfaces. Separate effectful adapters and composition roots from domain logic. Provide reusable safe paths for transactions, cancellation, retries and telemetry. Make boundaries visible in directory names and manifests; implement dependency checks at real build and runtime boundaries.

## Required evidence and acceptance
Compile or validate invalid inputs; exercise bypass attempts at trust boundaries; prove legal callers can use the supported path and legacy consumers remain compatible.

## Guardrails
Static visibility is not authorization. Dynamic loading, deserialization and reflection need explicit boundary verification.
