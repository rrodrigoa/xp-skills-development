# Reusable CLI tool blueprint

## When to load
Generating or refactoring a CLI over a library.

## Procedure
Design a thin parser and command dispatcher, typed request, reusable application service, output renderer and dependency composition. Define exit codes, stdout/stderr, JSON schema, noninteractive behavior, cancellation, configuration precedence and authorization for side effects.

## Required evidence and acceptance
CLI contract table, subprocess and direct invocation tests, invalid flags, machine output, cancellation and reusable service tests.

## Guardrails
Do not implement business rules in command handlers; no silent success or unexpected prompts in automation.
