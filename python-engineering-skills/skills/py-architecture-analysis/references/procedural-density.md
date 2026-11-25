# Procedural density and OO smells

## When to load
Investigating function-heavy Python modules.

## Procedure
Count top-level functions, classes, methods and static-only classes separately with scope. Find repeated mutable context parameters, shared global state, parallel dictionaries, type switches, repeated client injection, feature envy and duplicated rules. Group by invariant, lifecycle and callers, not by lexical names alone.

## Required evidence and acceptance
For each proposed object cite multiple operations, state ownership, invariant and a candidate interface; explicitly identify pure functions to preserve.

## Guardrails
Do not impose class/function ratios, static-method bans for justified utilities, or one class per file. Counts are triage only.
