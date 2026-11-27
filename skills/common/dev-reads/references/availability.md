# A — Availability and successful user journeys

## When to load
Measuring whether a capability works for users.

## Procedure
Choose event-based availability (good eligible outcomes divided by eligible outcomes) or time-based availability (good observed intervals divided by eligible observed intervals) according to the contract. Define good including correctness and possibly deadline; keep latency SLI separate if the policy calls for it. Use external synthetic probes to detect inability to reach ingress and low-traffic outages, ideally from relevant locations and authenticated paths. Reconcile passive user signals and probes as separate evidence rather than silently averaging them. Explicitly classify no traffic, missing data, planned exclusions and partial regional outage. For asynchronous work measure accepted-to-durable-completion or freshness, not acceptance alone. Distinguish capability availability from pod readiness and dependency availability.

## Required evidence and acceptance
Provide numerator, denominator, window, exclusion rationale, probe coverage and missing-data policy; test inaccessible ingress, empty traffic, partial outage and successful recovery.

## Guardrails
No requests or missing scrape does not mean 100% availability; a healthy process may serve broken functionality.
