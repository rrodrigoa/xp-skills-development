# Python deterministic tests and reproducible failures

## When to load
Testing nondeterministic behavior and rule enforcement.

## Implementation in the target project
Use dev-runtime-verification controlled-time and property-fuzz. Use pytest isolated fixtures, injected clock and RNG, asyncio events/barriers, Hypothesis generated examples and shrinking; record failing example and seed/tool version when available. Verify collection, skip/xfail reasons and real negative controls. Test checker failures and subprocess exit propagation separately.

## Required evidence and acceptance
Replay minimized failure; verify candidate test scope and exit status; run clean and installed-artifact suites where approved.

## Guardrails
Do not globally monkeypatch time or use retry plugins to convert flaky required failures into passes.
