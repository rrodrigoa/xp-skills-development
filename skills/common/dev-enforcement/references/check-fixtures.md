# Test the enforcement mechanism itself

## When to load
Adding or changing any required checker.

## Implementation in the target project
Create minimal intentionally invalid and valid fixtures independent of product code. Cover edge syntax, scope exclusions, disabled/missing tool, parse errors and runner exit propagation. For behavioral checks inject a representative regression or use a pre-fix revision. Verify fixture expectations and diagnostic IDs; include fixture execution in check's own CI.

## Required evidence and acceptance
Observed red for intended defect, green for valid input and explicit error for tool failure; report exact fixture count and check version.

## Guardrails
Never leave intentional failing fixtures in normal test discovery without isolation. A failed command for unrelated setup is not a valid negative control.
