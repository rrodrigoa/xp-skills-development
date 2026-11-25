# MCP tools and schemas

## Use when
Exposing reusable tools to agents.

## Avoid when
Large generic execute-anything tool or untyped result strings.

## Implementation
Define narrow tools with clear descriptions, typed schema, authorization and bounded inputs; map to application services; structured outputs and errors; version contracts.

## Verification and review
Test positive, negative, unauthorized and malformed requests; transport integration separately.
