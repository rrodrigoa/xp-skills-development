# API and adapter blueprint

## When to load
Exposing existing application capabilities over HTTP, RPC or another interface.

## Procedure
Map request schema to application types, authenticate and authorize independently, validate input, call the service, map errors/status and render output. Define versioning, idempotency, timeouts, pagination, resource bounds and tracing at boundary.

## Required evidence and acceptance
Contract, compatibility, unauthorized, malformed input and downstream failure cases; shared service tests independent of transport.

## Guardrails
Do not duplicate policy across endpoints. Avoid claiming an operation is idempotent without defining side-effect semantics.
