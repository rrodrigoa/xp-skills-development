# Python packaging and distribution

## Shared guidance
dev-delivery: packaging, release, ci; dev-quality-gates: release-gate

## When to load
Publish package or CLI.

## Language-specific decisions
Verify PEP 517 build artifacts, metadata, version, data files, entry points and optional types; use approved registry and trusted publishing where configured. Test clean install from wheel and build from sdist.

## Verification and evidence
Record hashes, artifact provenance, supported interpreter matrix and registry permissions; no publication without authority.

## Avoid
Testing source imports only, publishing secrets or mutable release artifacts.
