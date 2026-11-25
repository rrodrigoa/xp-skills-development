# Security and trust-boundary gate

## When to load
Input, authorization, secrets, dependencies or external actions are affected.

## Procedure
Trace trust boundaries and identify affected threat scenarios. Inspect authentication, authorization, validation, path/command handling, resource limits, logging redaction and least privilege. Require negative/adversarial tests and relevant security scan results under policy.

## Required evidence and acceptance
Threat-to-control mapping, concrete evidence of authorization enforcement, scan findings with triage, tested denial paths.

## Guardrails
Never rely on prompt instructions as authorization; don't reveal secrets or execute untrusted payloads outside approved sandbox. No score compensates for confirmed prohibited side effects.
