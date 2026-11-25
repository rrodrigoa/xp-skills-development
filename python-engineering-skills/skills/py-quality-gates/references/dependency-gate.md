# Supply-chain and dependency gate

## When to load
Dependencies, build metadata or lockfiles change.

## Procedure
Check necessity, direct/transitive impact, supported versions, provenance, license policy, vulnerability findings, reproducibility and lockfile consistency. Verify optional dependency behavior and clean environment installation if required.

## Required evidence and acceptance
Dependency diff, rationale, scan/date and triage, license compatibility under policy and build evidence.

## Guardrails
Do not invent CVE or license conclusions. Unavailable scan is UNKNOWN when required; exceptions need owner and expiry.
