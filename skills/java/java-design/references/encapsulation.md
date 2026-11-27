# Java visibility, packages and modules

## Shared guidance
oo-design: package-boundaries, public-api

## When to load
Define public and internal boundaries.

## Language-specific decisions
Default to least visibility: private state, package-private implementation when practical, public only for contract. Use packages organized by capability; use JPMS exports/opens only when the project uses modules. Reflection and serialization may bypass ordinary visibility; design explicit boundaries and limit reflective access.

## Verification and evidence
Inspect public signatures, module exports and actual consumer builds; verify no mutable collections escape.

## Avoid
Public fields or public classes for every helper; adding JPMS without a real need.
