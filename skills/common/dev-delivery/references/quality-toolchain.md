# Static analysis and quality toolchain

## Use when
Standardizing local and CI checks.

## Avoid when
Introducing overlapping tools or mass unrelated formatting.

## Implementation
Use the approved formatter, linter, compiler or type checker and test framework. Adopt gradually for legacy; branch coverage threshold is project policy.

## Verification and review
Run format check, lint, type check, tests and build; report exact commands.
