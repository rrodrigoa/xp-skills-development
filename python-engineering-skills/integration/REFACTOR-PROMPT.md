# Prompt for an existing procedural Python repository

Use `py-engineering` and `py-refactoring`. Inspect the repository, public APIs, tests, packaging and existing abstractions before editing. Load only the appropriate architecture, pattern and verification references.

1. Produce a concise inventory of modules with misplaced behavior, shared mutable state, repeated context arguments, duplicated logic, weak domain representation, unclear interfaces or infrastructure leakage. Cite paths and concrete symbols, not just counts.
2. Propose a staged target design with owners, public contracts, dependency direction, reusable components and relevant pattern choices. Justify why each abstraction is needed; retain pure functions where appropriate.
3. Establish characterization tests and record baseline checks. Refactor one cohesive slice at a time; preserve public behavior, error semantics and compatibility unless I approve changes. Do not move procedural code into static-only classes.
4. Add focused behavioral, contract, negative and adversarial tests as relevant. Run available formatting, lint, type, tests and build gates. Review the resulting diff for duplication, incomplete work and boundary violations.
5. Deliver a concise change report including commands and actual results, remaining architectural risks and unverified checks. Do not claim success for unexecuted checks. Do not push or publish without authorization.

If the requested scope is too large, complete a coherent verified slice and explicitly enumerate remaining work. No placeholder implementations or comments that substitute for requested behavior.
