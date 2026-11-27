# Control clocks, randomness and scheduling

## When to load
Flaky time-based or concurrent behavior.

## Implementation in the target project
Inject clock/random/scheduler at meaningful boundaries; use fake time for timeout/retry tests and retain real integration checks. Set seeds and deterministic fixture order; drive concurrency with barriers or explicit events rather than sleeps. Test cancellation, races, expiration, DST/timezone where relevant; record platform and schedule assumptions.

## Required evidence and acceptance
Known timing regression reproduced reliably; tests do not depend on arbitrary delays; real runtime checks exercise actual scheduling risks.

## Guardrails
A single deterministic schedule cannot prove race freedom. Do not freeze time in tests meant to measure performance.
