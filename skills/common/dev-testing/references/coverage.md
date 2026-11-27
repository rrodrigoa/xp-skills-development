# Coverage and mutation testing

## Use when
Quality gates and regression risk.

## Avoid when
Treating coverage percentage as correctness or adding meaningless asserts.

## Implementation
Measure branch coverage, prioritize risky gaps; apply only project-approved thresholds; calibrate any proposed floor before adoption; use mutation testing selectively; document exclusions with rationale.

## Verification and review
Run configured threshold; prove uncovered critical paths are tested or explicitly tracked.
