# Mutation testing and flaky-test assessment

## When to load
Assessing whether tests detect defects or produce unstable signals.

## Procedure
For mutation, inspect surviving meaningful mutants, equivalent mutants and timeouts separately; choose risk-focused scope. For flakiness, record same-revision repeated runs, environment, observed failures and seeds. Track quarantine owner, expiry and compensating coverage.

## Required evidence and acceptance
Mutation or flake evidence, classification, repeatability, impact and remediation; apply calibrated policy only.

## Guardrails
Do not hide nondeterministic failures or delete meaningful assertions. Do not demand mutation score for unsupported projects.
