# Java reproducible verification toolchain

## When to load
Implementing local and CI quality checks.

## Implementation in the target project
Use dev-enforcement ci-enforcement and check-fixtures. Respect Maven/Gradle wrapper, toolchain and dependency policy; use existing compiler, Checkstyle, Error Prone, PMD, SpotBugs or ArchUnit as appropriate. For custom checks choose supported extension mechanism and fixture it. Verify lifecycle executes integration tests and expected artifact; check installed/consumed JAR independently.

## Required evidence and acceptance
Bad fixture fails required command, good fixture passes, exact JDK/build/tool versions and report counts retained.

## Guardrails
Do not assume compile success implies all test phases ran; no unapproved plugin or branch-rule changes.
