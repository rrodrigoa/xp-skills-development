# Protect checks and policy from candidate manipulation

## When to load
Agent modifies tests, lint, CI or acceptance policy.

## Implementation in the target project
Classify trusted policy and checker configuration separately from candidate product changes. Require independent review of changes to fixtures, expected results, suppressions, coverage exclusions, required contexts, proof assumptions and build filters. Verify actual test count and checked scope, not only exit status; evaluate changed checker against approved base controls where feasible. Invalidate evidence after any candidate change.

## Required evidence and acceptance
Diff and provenance identify every altered control; bypass fixtures or independent rerun detect weakening; unauthorized changes are reported under GOV-02.

## Guardrails
Legitimate test or policy evolution is allowed with independent approval. Do not run untrusted candidate code with privileged secrets.
