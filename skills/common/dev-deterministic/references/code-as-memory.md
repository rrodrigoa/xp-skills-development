# Codebase as reusable agent context

## When to load
Agents keep copying bad examples.

## Implementation in the target project
Search actual callers, similar features and review history. Identify canonical implementations, deprecated paths, examples and copied workarounds. Choose one supported way to do each recurring operation, expose it through an understandable API, and migrate representative callers. Remove obsolete paths after compatibility review; if retained, isolate and prevent new callers. Keep discovery pointers short and link only the canonical example.

## Required evidence and acceptance
Search confirms no new references to deprecated paths; supported examples build and test; a fresh agent task uses the intended route without needing a bespoke prompt.

## Guardrails
Do not remove compatibility shims or historical migrations needed by supported clients. Avoid refactoring unrelated code just to beautify context.
