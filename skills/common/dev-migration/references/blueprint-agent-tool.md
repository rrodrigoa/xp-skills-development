# MCP and autonomous tool blueprint

## When to load
Exposing a reusable capability to agents.

## Procedure
Declare tool purpose, typed input/output, permissions, trusted execution boundary, side effects, resource limits, error semantics, cancellation and trace IDs. Separate model selection from independent authorization and implementation; use application service shared with other interfaces.

## Required evidence and acceptance
Positive, invalid, unauthorized and adversarial scenarios; traceable side effects and response schema; explicit no-op/dry-run semantics if supported.

## Guardrails
Treat model inputs and tool results as untrusted. No self-approved authorization or unrestricted remote execution.
