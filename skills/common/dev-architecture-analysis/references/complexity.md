# Complexity and nesting

## When to load
Reviewing complicated control flow or hotspots.

## Procedure
Use a stated cyclomatic metric/tool convention; report per-function complexity, nesting and size separately. Inspect exceptional and asynchronous paths, branch interaction, and whether variants are policy or state. Compare changed functions to baseline and examine coverage of high-risk decisions.

## Required evidence and acceptance
List locations, decision paths, metric definition and tests or refactoring candidates; highlight changed complexity rather than only totals.

## Guardrails
Cognitive complexity and cyclomatic complexity are different; avoid arbitrary limits, moving branches into helpers to game scores, or conflating size with defects.
