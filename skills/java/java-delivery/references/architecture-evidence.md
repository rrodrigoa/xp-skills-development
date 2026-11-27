# Java build boundaries and architecture tests

## Shared guidance
dev-architecture-analysis: architecture-contracts, fitness-functions; dev-quality-gates: architecture-gate

## When to load
Enforce approved dependency direction.

## Language-specific decisions
Inspect Maven/Gradle module graph and class/package dependency evidence. Use ArchUnit or jdeps for appropriate checks, separating compile-time dependency and runtime injection. Map generated/third-party exclusions to approved scope; treat missing module reports as unknown.

## Verification and evidence
Report revision, selected artifacts, rule IDs, violations and baseline comparison.

## Avoid
Suppressing new cycles or using package naming as sole proof of architecture.
