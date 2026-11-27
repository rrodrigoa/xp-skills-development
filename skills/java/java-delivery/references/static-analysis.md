# Java compiler and static analysis gates

## Shared guidance
dev-delivery: quality-toolchain; dev-quality-gates: static-quality

## When to load
Configure or interpret Java static checks.

## Language-specific decisions
Use configured javac warnings, Checkstyle/Spotless, SpotBugs, Error Prone, PMD or approved tools for distinct concerns. Nullability and architecture rules may be separate. Record source target, exclusions and incremental versus full scope; review every new suppression.

## Verification and evidence
Capture tool versions, build logs, exit codes and diagnostics at reviewed revision; no unapproved severity reductions.

## Avoid
Treating compiler success as complete static verification or enabling all tools without policy.
