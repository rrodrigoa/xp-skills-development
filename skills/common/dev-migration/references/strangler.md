# Incremental subsystem replacement

## When to load
Replacing a legacy service or module without a big-bang rewrite.

## Procedure
Place a stable boundary in front of old/new implementations; route low-risk use cases first. Define data ownership, consistency, routing and monitoring. Migrate vertical slices with separate failure recovery and final retirement criteria.

## Required evidence and acceptance
Routing map, contract tests per slice, operational parity and verified fallback or forward recovery.

## Guardrails
Avoid hidden distributed transactions and unbounded dual-write; do not retire legacy consumers without evidence.
