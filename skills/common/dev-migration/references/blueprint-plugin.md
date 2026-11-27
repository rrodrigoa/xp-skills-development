# Plugin and extension blueprint

## When to load
Designing selectable providers or a plugin architecture.

## Procedure
Identify real extension axis and consumer-owned protocol. Define discovery mechanism, version/capability checks, explicit registry or entry point, lifecycle and isolation, configuration and failure behavior. Compose at startup; test each provider with common contract.

## Required evidence and acceptance
Plugin registration, unknown and incompatible plugin cases, lifecycle cleanup and substitution tests.

## Guardrails
Do not load untrusted plugin code by default. Avoid speculative plugin frameworks when one stable implementation suffices.
