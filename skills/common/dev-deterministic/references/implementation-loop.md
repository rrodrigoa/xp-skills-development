# Bounded implementation and verification inner loop

## When to load
Any nontrivial coding task.

## Implementation in the target project
Freeze scope, base revision, policy and acceptance. Inspect existing implementation and approved examples. Write a failing test for a defect or a checkable feature oracle; implement the smallest coherent slice. Run fast constraints, then behavioral and runtime checks; repair causal failures and rerun affected checks. Inspect diff for unauthorized policy edits. Freeze candidate and hand off independent evidence. Stop at explicit budget or permission boundaries.

## Required evidence and acceptance
Record iterations, test evidence, revision and unresolved failures. Independent reviewer can reproduce required checks; no optimistic completion.

## Guardrails
Do not loop indefinitely or alter oracle to match output; escalate an ambiguous requirement or unavailable dependency.
