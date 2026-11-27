# READS, RED, USE and golden signals

## When to load
Selecting complementary monitoring frameworks.

## Procedure
Use READS at service/user-journey boundaries. RED (rate, errors, duration) is a convenient request-oriented subset; add availability as an explicit outcome and saturation for capacity. USE (utilization, saturation, errors) targets each resource; use it to investigate causes when READS shows impact. Google SRE golden signals cover traffic, errors, latency and saturation. Build one shared semantic contract, then project these views without duplicate instruments. Associate service symptoms with dependency and resource signals through common service identity and time range.

## Required evidence and acceptance
A matrix shows which questions each view answers, which instruments are reused and which gaps require new telemetry.

## Guardrails
Do not treat frameworks as competing standards or assume a resource error necessarily means user impact.
