# Property-based and stateful fuzz verification

## When to load
Large input space or interaction sequences.

## Implementation in the target project
Specify invariants independently, construct valid and invalid generators, model allowed actions and preconditions, bound search time and sequence length. Use shrinking/minimization and capture seed, tool version and minimized failing trace. For UI use compatible stateful tools (e.g., Bombadil if approved) and reset app after each run. Turn failures into deterministic regression cases before fixing.

## Required evidence and acceptance
Known injected defect is found by suitable test or regression; failing seed replays; evidence reports search budget and coverage limits.

## Guardrails
No finite fuzz run proves absence of bugs. Do not fuzz production or third-party systems without authorization.
