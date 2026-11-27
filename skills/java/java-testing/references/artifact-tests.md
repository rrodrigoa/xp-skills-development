# Java installed artifact and compatibility tests

## Shared guidance
dev-testing: e2e, contract; dev-quality-gates: test-execution-gate, compatibility-gate

## When to load
Verify JAR/library/CLI.

## Language-specific decisions
Test published artifact in fresh consumer project or controlled launcher; test supported JDK versions and classpath/module path as appropriate. Check resources, service provider files, manifests, native or runtime dependencies.

## Verification and evidence
Record build artifact hash, consumer compile/run, supported matrix, skips and exit results.

## Avoid
Testing IDE classpath only or reporting untested JDKs as compatible.
