# Custom lint and actionable diagnostics

## When to load
Repeated mechanical mistakes.

## Implementation in the target project
Use existing lint extension or syntax-aware analysis; resolve symbols/import aliases where needed, match the smallest prohibited construct, and report path, rule ID, rationale and supported replacement. For framework-only APIs scope by trusted module ownership. Add fixtures for aliases, nested scopes, comments/strings, legitimate exemptions and malformed input. Test any autofix for idempotence and behavior.

## Required evidence and acceptance
Known violation fails; harmless lookalike passes; rule diagnostics guide repair without a long prompt; test lint implementation in CI.

## Guardrails
Lint cannot prove runtime correctness; avoid unsafe automatic fixes and unchecked blanket suppressions.
