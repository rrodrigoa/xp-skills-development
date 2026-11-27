# Machine-checkable rule specification

## When to load
Converting a policy into a check.

## Implementation in the target project
Assign stable contract ID under existing gate; specify exact scope, excluded generated/vendor paths, permitted exceptions, forbidden example, allowed example, diagnostic, severity, version and owner. Select cheapest reliable analysis (compiler, AST, dependency graph, behavior test); define known false negatives, dynamic edges and failure semantics. Separate rule code from candidate-controlled configuration.

## Required evidence and acceptance
Good/bad/edge fixtures and clean invocation show rule detects intended defect with stable diagnostic and nonzero failure exit. Missing tool or parse failure must not pass.

## Guardrails
Do not encode subjective style or semantic correctness as a brittle lexical regex. Keep qualitative review if reliable automation is unavailable.
