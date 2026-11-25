# Procedural service to domain/application objects

## When to load
Shared context and utility functions implement a service lifecycle.

## Procedure
Identify lifecycle and invariants from callers and mutation sites. Extract meaningful value types and state owner; move behavior to owner, delegate I/O through narrow ports, keep orchestration in application service. Maintain legacy facade while migrating clients and remove duplicated rules.

## Required evidence and acceptance
Characterization tests, independent instances, invariant tests, unchanged external behavior and lower implicit state sharing.

## Guardrails
Pure helpers stay functions. Do not create a god service or a repository for in-memory state without a need.
