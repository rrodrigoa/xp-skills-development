# Dependency injection and composition root

## Use when
Services need storage, clock, transport or policy.

## Avoid when
A DI container for a small dependency graph.

## Implementation
Constructor-inject required collaborators; use explicit factory/bootstrap wiring, deterministic resource scopes for lifetime; avoid hidden service locators.

## Verification and review
Construct isolated services and verify cleanup of owned resources.
