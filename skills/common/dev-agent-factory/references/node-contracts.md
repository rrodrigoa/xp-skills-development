# Typed node and tool contracts

## When to load
Implementing graph nodes or agent tools.

## Implementation in the target project
Specify node input/output schema, authority, side effects, idempotency key, deadline, resource budget, retry classification and output validation. Treat model text and tool payloads as untrusted; host verifies declared artifacts and state transitions. Use reusable deterministic services and adapters; maintain error causes and READS instrumentation. Checkpoint versioned state and isolate workspaces.

## Required evidence and acceptance
Contract tests cover invalid output, unauthorized action, duplicate invocation, timeout, resume and terminal failures; host rejects malformed transition requests.

## Guardrails
Do not rely on self-reported completion or allow model to grant itself capabilities.
