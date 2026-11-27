---
name: dev-enforcement
description: "Design and validate machine-enforced architecture rules, custom lint, type constraints, test oracles, CI checks and anti-bypass policies in target projects."
---
# Executable engineering enforcement

Use dev-engineering for routing and dev-governance for approved policy. This is guidance only: implement authorized constraints, checks and tools in the consuming repository. Load one or two matching cards first. Use dev-quality-gates for independent decisions; no self-approval or missing-evidence pass.

## Reference selector
- [Machine-checkable rule specification](references/rule-contract.md) — Converting a policy into a check.
- [Custom lint and actionable diagnostics](references/custom-lint.md) — Repeated mechanical mistakes.
- [Executable architecture fitness rules](references/architecture-fitness.md) — Layer, module or dependency constraints.
- [Type and compiler constraints](references/types-and-invariants.md) — Invalid states, wrong units or unchecked variants.
- [Test the enforcement mechanism itself](references/check-fixtures.md) — Adding or changing any required checker.
- [Framework and paved-path APIs](references/architecture-framework.md) — Recurring decisions are hard for feature agents.
- [Local checks and protected CI enforcement](references/ci-enforcement.md) — Moving a useful check into a required gate.
- [Protect checks and policy from candidate manipulation](references/anti-bypass.md) — Agent modifies tests, lint, CI or acceptance policy.
- [Baseline and ratchet enforceable debt](references/baseline-ratchet.md) — Existing code fails a new rule.
- [Revision-bound machine evidence contract](references/verification-evidence.md) — A tool result feeds a gate or automated repair.
- [Worked rule lifecycle: forbidden dependency](references/worked-rule.md) — Adopting the first architecture fitness rule.
