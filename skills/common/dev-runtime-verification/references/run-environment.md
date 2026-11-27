# Controlled runnable application environment

## When to load
Preparing real behavior verification.

## Implementation in the target project
Determine approved start/build command, dependency services, isolated profile/data, supported platform and credentials. Establish readiness using meaningful health checks; bound startup, execution and shutdown. Reset data per scenario; record process IDs and cleanup. Test installed artifact when release contract requires it; include actual integration dependencies where needed.

## Required evidence and acceptance
Application identity and readiness verified; feature runs against candidate, not stale process; cleanup and failed startup tested.

## Guardrails
Do not claim mock-only run validates deployed behavior. Network/environment unavailability is UNKNOWN for required evidence.
