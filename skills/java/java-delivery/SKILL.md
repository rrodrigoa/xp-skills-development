---
name: java-delivery
description: "Build and release Java projects; manage dependencies, compatibility, static checks and revision-bound evidence."
---
# Java Delivery

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: dev-delivery and applicable dev-quality-gates. Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [Java project layout and JDK support](references/project-layout.md) — New module or build layout.
- [Maven dependency and lifecycle management](references/maven.md) — Build Maven project.
- [Gradle toolchains and dependency management](references/gradle.md) — Build Gradle Java project.
- [Java compiler and static analysis gates](references/static-analysis.md) — Configure or interpret Java static checks.
- [Java binary, source and behavioral compatibility](references/compatibility.md) — Change published Java API.
- [Java packaging and releases](references/release.md) — Publish library or executable.
- [Java build boundaries and architecture tests](references/architecture-evidence.md) — Enforce approved dependency direction.

- [Java reproducible verification toolchain](references/deterministic-ci.md) — Implementing local and CI quality checks.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.
