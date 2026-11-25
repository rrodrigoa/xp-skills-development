# Coupling and dependency stability

## When to load
Evaluating dependency concentration or package fragility.

## Procedure
For each selected unit count distinct incoming dependencies (Ca) and outgoing dependencies (Ce), using a consistent graph and excluding self edges. Report instability as Ce divided by the sum of Ca and Ce; mark isolated units undefined. Inspect change coupling separately from import coupling; identify concrete volatile dependencies at stable boundaries.

## Required evidence and acceptance
Give counts, definition, revision, edge types and ranked hotspots with source examples; compare like-for-like baseline.

## Guardrails
High fan-in can indicate useful reuse; high fan-out can be legitimate orchestration. No universal threshold or automatic inversion based on a ratio.
