# Packaging and release readiness gate

## When to load
A distributable artifact or release is proposed.

## Procedure
Check version consistency, changelog, build provenance, wheel/sdist or deployment artifact, clean install, supported versions and public entry points. Inspect upgrade, migration and recovery guidance. Confirm publish permissions and approval separately.

## Required evidence and acceptance
Artifact identity, build/installation results, compatibility and release checklist; exact release candidate revision.

## Guardrails
Build success is not publication. Do not push tags, upload artifacts or deploy without authorization.
