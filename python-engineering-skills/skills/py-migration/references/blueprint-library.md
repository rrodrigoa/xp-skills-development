# Reusable Python library blueprint

## When to load
Designing or extracting a library from application code.

## Procedure
Define consumer-facing types and operations, versioned contract, stable exceptions, dependency policy and optional integrations. Separate pure core from stateful services and I/O adapters; expose explicit resource ownership and composition. Describe packaging, documentation and installed-distribution checks.

## Required evidence and acceptance
Consumer use cases, import/API inventory, positive/negative contract tests, installed package verification and compatibility policy.

## Guardrails
Do not leak CLI/API framework types or credentials into core. Avoid unnecessary abstractions or forced src layout for tiny scripts.
