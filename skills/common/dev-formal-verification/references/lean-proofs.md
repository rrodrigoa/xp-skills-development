# Lean algorithm proof and proof hygiene

## When to load
Mathematical algorithm with precise specification.

## Implementation in the target project
Define mathematical inputs, output and theorem independent of current code. Specify preconditions, termination and numeric representation; prove relevant lemmas and theorem using approved Lean version. Inspect dependencies and axioms, reject sorry/admit or unapproved axioms; ensure theorem is nontrivial and not weakened. If implementation is separate, define mapping and test boundary/overflow cases.

## Required evidence and acceptance
Kernel-checked theorem, tool version, approved axiom inventory, theorem statement and linkage to real algorithm; broken claim fails.

## Guardrails
A proof of a mathematical model is not a proof of arbitrary Java/Python implementation, UI rendering or external effects.
