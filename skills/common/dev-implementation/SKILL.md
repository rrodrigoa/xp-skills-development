---
name: dev-implementation
description: "Implement professional libraries, APIs, CLI tools, naming, type contracts, errors, documentation and reusable components."
---
# Implementation

Read existing build manifest and style. Define public contract before coding. Separate domain behavior from I/O, validation, rendering and CLI parsing. Use explicit dependencies, meaningful names and typed boundaries. Keep examples and documentation current. Avoid broad catches, import-time effects and speculative abstractions. Verify public behavior with tests.

## Reference selector
Read only relevant files from this list.

- [Naming conventions](references/naming.md) — Creating or reviewing identifiers.
- [Functions versus methods](references/functions-methods.md) — Choosing location of behavior.
- [Type contracts and generics](references/typing.md) — Public API, complex collections or polymorphic boundaries.
- [Data models and validation](references/models-validation.md) — Structured input crosses a trust or serialization boundary.
- [Exceptions and error contracts](references/errors.md) — Operations can fail or cross a boundary.
- [Comments and docstrings](references/comments-docstrings.md) — Public contracts, non-obvious invariants or tradeoffs.
- [Module cohesion and reuse](references/module-design.md) — Similar helpers appear across modules.
- [CLI architecture](references/cli-design.md) — Building or extending a command-line tool.
- [Interactive and machine-readable CLI](references/cli-interactive.md) — Tool used by humans and agents.
- [CLI plugins and extension points](references/cli-plugins.md) — Third parties add commands or backends.
- [Library and HTTP API design](references/api-design.md) — External consumers call stable interfaces.
- [Configuration and settings](references/configuration.md) — Settings vary by environment or invocation.
- [Serialization and schemas](references/serialization.md) — Persistent or wire formats need compatibility.
- [Resource lifecycle and deterministic cleanup](references/resource-lifecycle.md) — File, socket, session, lock or transaction ownership.
- [Logging and diagnostics](references/logging.md) — Library or tool needs actionable diagnostics.

- [Cross-language contracts](references/cross-language-contracts.md) — Load for this specific topic.
