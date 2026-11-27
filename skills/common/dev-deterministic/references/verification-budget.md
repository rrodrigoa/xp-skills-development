# Verification-first token and compute budget

## When to load
Planning agent work or optimizing throughput.

## Implementation in the target project
Estimate risk and allocate budget to independent verification before generation. Use fast checks during edits and targeted integration/runtime checks per slice; run full required checks before eligibility. Reserve resources for counterexamples and debugging. Capture actual generation, verification and repair usage separately; compare escaped defects and cost per accepted change.

## Required evidence and acceptance
Budget and stop conditions are defined; evidence shows required checks ran without truncation; report cost and residual risk.

## Guardrails
The speaker's cited verification share is an anecdote, not a mandatory ratio. Never skip required checks to satisfy a token budget.
