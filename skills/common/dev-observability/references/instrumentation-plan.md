# Observability-first feature design

## When to load
Designing a service, feature, migration or refactor.

## Procedure
Read the READS contract and inspect current instrumentation and monitoring consumers. For each meaningful boundary list diagnostic questions, terminal outcomes, dependencies, state transitions and capacity risks. Map each to an instrument, structured event, span or probe with owner and reason. Choose auto instrumentation for supported transport edges and manual instrumentation for domain semantics. Reuse existing instruments if meaning matches; plan versioned schema changes if not. Include telemetry cost, trust/privacy, failure isolation, dashboards, alert intent, test cases and rollout in acceptance criteria. Prefer one coherent vertical slice: emitted measurement, exported sample, query, dashboard and actionable response.

## Required evidence and acceptance
Produce an instrumentation plan tied to changed operation contracts and a verification matrix covering success, failure, timeout, cancellation, retry and telemetry outage.

## Guardrails
Do not add a log at every function entry or create an observability framework before inspecting existing facilities.
