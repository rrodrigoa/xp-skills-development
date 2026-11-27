---
name: py-design
description: "Apply Python idioms for OO representation, interfaces, patterns, dependency injection and architecture inspection."
---
# Python Design

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: oo-design and oo-patterns (or dev-architecture-analysis for audits). Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [Python object and value representation](references/object-representation.md) — Domain entities, immutable values and transport models.
- [Protocols, ABCs and duck typing](references/interfaces.md) — Define substitutable ports or plugins.
- [Python visibility and descriptors](references/encapsulation.md) — Protect state and published interfaces.
- [Python creational pattern mapping](references/creational-patterns.md) — Construct or scope objects.
- [Python structural pattern mapping](references/structural-patterns.md) — Adapt or compose abstractions.
- [Python behavioral pattern mapping](references/behavioral-patterns.md) — Dispatch, iterate, compose workflows or vary policies.
- [Python enterprise pattern mapping](references/enterprise-patterns.md) — Persistence, pipelines, distributed operations or resource reuse.
- [Python dependency and ownership analysis](references/architecture-inspection.md) — Audit modules and hidden coupling.

- [Python enforceable API and architecture boundaries](references/deterministic-boundaries.md) — Prevent invalid calls and cross-layer imports.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.
