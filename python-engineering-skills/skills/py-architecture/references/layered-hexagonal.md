# Layered and hexagonal architecture

## Use when
Domain logic coupled to frameworks and external systems.

## Avoid when
A one-file script without evolving business rules.

## Implementation
Keep domain inward, application orchestrates ports, adapters translate external models, bootstrap wires. Prevent inward modules importing adapters.

## Verification and review
Inspect import graph and test domain without framework initialization.
