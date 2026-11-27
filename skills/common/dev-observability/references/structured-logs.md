# Structured logs, events and diagnostic context

## When to load
Designing logs for humans and machines.

## Procedure
Emit stable event names with timestamp, severity, service identity, operation, outcome, bounded error category, trace/span correlation, and meaningful safe context. Use structured fields rather than fragile string parsing; keep human message concise and explain why the event matters. Log exceptions where owned/handled or terminally reported, not at every rethrow. Distinguish audit events from operational debug logs: retention, access and delivery guarantees may differ. Use dynamic verbosity or rate-limiting with dropped-log evidence. Preserve machine-readable CLI stdout. Avoid payload dumps and unbounded indexed identifiers. Never log secrets, auth headers or raw prompts by default.

## Required evidence and acceptance
Exercise representative normal and error flows; query stable fields and correlate traces; inspect redaction, logging levels, duplicate events, rate limiting and output separation.

## Guardrails
Do not rely on log text as the only authoritative counter or log full stack/payload for every expected rejection.
