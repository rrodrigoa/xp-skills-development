# Architecture boundary and drift gate

## When to load
Imports, domain ownership or module boundaries change.

## Procedure
Use the approved architecture contract and matched base/head graph from `py-architecture-analysis`. Check new or worsened forbidden edges, runtime cycles, leakage of framework types and duplicate policy ownership. Record inherited debt and approved exceptions separately. Inspect dynamic dependencies where relevant.

## Required evidence and acceptance
Contract ID, edge or behavioral evidence, scope, baseline delta and result for each rule.

## Guardrails
Class counts, cohesion and coupling heuristics alone cannot block. No architecture contract invented retrospectively by reviewer.
