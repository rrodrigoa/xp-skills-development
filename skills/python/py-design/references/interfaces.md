# Protocols, ABCs and duck typing

## Shared guidance
oo-design: protocols-abcs, solid-isp, solid-lsp

## When to load
Define substitutable ports or plugins.

## Language-specific decisions
Prefer a narrow consumer-owned typing.Protocol when structural typing fits; ABC for nominal membership or meaningful shared lifecycle. Use callable contracts for simple algorithms and constructor injection for long-lived collaborators. Runtime-checkable protocols do not prove signatures or behavior.

## Verification and evidence
Run configured type checker and the same behavioral contract tests against each adapter.

## Avoid
Interface for every class; inheritance purely to satisfy type checker.
