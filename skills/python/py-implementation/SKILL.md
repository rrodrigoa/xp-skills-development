---
name: py-implementation
description: "Implement Python naming, types, validation, documentation, APIs, CLI, plugins and source refactoring."
---
# Python Implementation

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: dev-implementation and dev-refactoring. Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [Python naming and layout](references/naming.md) — Add or rename Python symbols.
- [Python type contracts](references/typing.md) — Public APIs and dynamic boundaries.
- [Dataclasses and boundary validation](references/models-validation.md) — Parse external data or establish domain invariants.
- [Python docstrings and comments](references/comments-docstrings.md) — Document a public interface or non-obvious tradeoff.
- [Python exception design](references/errors.md) — Define and translate failures.
- [Python CLI and entry points](references/cli.md) — Implement or refactor CLI.
- [Python plugin discovery](references/plugins.md) — Discover external providers.
- [Python serialization and boundaries](references/serialization.md) — Serialize or exchange persisted data.
- [Python refactoring mechanics](references/refactoring-mechanics.md) — Move or rename functions, types or packages.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.

- [Python agent and MCP adapter implementation](references/agent-tools.md) — Implementing Python agent, LLM and MCP adapters.
