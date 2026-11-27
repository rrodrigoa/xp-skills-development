# Formal specification and invariant inventory

## When to load
Designing safety-critical state or algorithm.

## Implementation in the target project
Write precise state variables, initial conditions, transitions, input domains and assumptions. Distinguish safety (forbidden reachable states), liveness (eventual progress under stated fairness), pre/postconditions and resource bounds. Review specification against user intent before encoding; include intentionally violated model to validate checker.

## Required evidence and acceptance
Owner-reviewed property inventory, versioned spec, counterexample from broken variant and acceptance criteria mapped to implementation.

## Guardrails
Do not encode requirement as assumption or make impossible initial state that proves everything vacuously.
