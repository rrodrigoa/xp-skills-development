# Packaging and public distributions

## Use when
Publishing reusable library or CLI.

## Avoid when
Depending on source-tree imports or undeclared files.

## Implementation
Use the native build system, metadata and distribution entry points; include required runtime resources and public type information where applicable. Verify each published artifact independently.

## Verification and review
Run the configured build, inspect artifacts, consume in a clean environment and smoke test.
