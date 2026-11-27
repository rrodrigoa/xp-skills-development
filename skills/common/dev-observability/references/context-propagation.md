# Context propagation and correlation

## When to load
Crossing process, thread, coroutine or message boundaries.

## Procedure
Use the approved propagation format (commonly W3C Trace Context) and framework APIs to inject/extract context across HTTP, RPC and messaging. Separate trace context from authorization and business identity; baggage is untrusted and can cross boundaries, so allowlist and bound it. Handle missing, malformed and untrusted incoming context safely; enforce tenant boundaries. Propagate across executors, async tasks, queues and retries deliberately, restoring/clearing context at completion. Link causally related background jobs when appropriate rather than retaining a stale parent indefinitely. Do not let correlation identifiers become metric labels.

## Required evidence and acceptance
Test across services, task reuse, concurrent tenants, missing/malformed headers, cancellation and retries; verify no context leakage and correct trace/log correlation.

## Guardrails
Do not trust trace IDs or baggage for identity or permissions.
