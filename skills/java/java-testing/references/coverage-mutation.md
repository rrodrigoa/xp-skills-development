# JaCoCo and mutation testing

## Shared guidance
dev-testing: coverage, property; dev-quality-gates: coverage-gate, mutation-flakiness

## When to load
Assess Java test quality.

## Language-specific decisions
Record JaCoCo instruction/branch/line metrics separately; identify aggregate module reports and generated exclusions. Use approved jqwik for properties or PIT for mutation when policy requires; inspect equivalent or timed-out mutants.

## Verification and evidence
Capture exact build revision, tool versions, counters and module denominators, seeds and surviving mutant evidence.

## Avoid
Equating Java branch coverage with Python branch coverage or excluding failures to meet target.
