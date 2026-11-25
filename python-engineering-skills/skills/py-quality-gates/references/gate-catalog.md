# Stable gate identifiers and default enforcement

## When to load
Selecting which criteria apply to a project or PR.

## Procedure
Use the catalog in this card as the common identifier registry. Project owners choose required checks and applicability using the project governance profile; do not invent additional mandatory numeric limits. For every activated rule record enforcement mode and evidence contract.

## Required evidence and acceptance
Every gate references a stable ID, approved policy and evidence. Reviewers can independently reproduce decision logic.

## Guardrails
If no approved profile exists, present advisory findings and HOLD any requested authoritative merge recommendation; never self-authorize thresholds.

## Rule registry
Default classifications are recommendations for adoption, not automatically active project rules. R = recommended required when applicable; A = advisory until the project adopts an objective rule. The profile must explicitly bind scope, evidence and thresholds. GOV-01 and GOV-02 are nonwaivable integrity prerequisites for any authoritative recommendation.

| ID | Criterion | Default | Detailed card |
|---|---|---|---|
| GOV-01 | Approved policy and revision-bound evidence | R | [Evidence](evidence.md) |
| GOV-02 | No manipulation of checks or self-approval | R | [Review integrity](review-integrity.md) |
| ARCH-01 | Approved dependency and ownership contracts | R | [Architecture](architecture-gate.md) |
| ARCH-02 | Semantic reuse and coherent object ownership | A | [Reuse](reuse-gate.md) |
| ARCH-03 | Complexity and maintainability regression | A | [Complexity](complexity-gate.md) |
| API-01 | Supported public compatibility | R | [Compatibility](compatibility-gate.md) |
| TEST-01 | Required tests executed successfully | R | [Execution](test-execution-gate.md) |
| TEST-02 | Required behavior and risk coverage | R | [Quality](test-quality-gate.md) |
| TEST-03 | Approved coverage floors and regression limits | A | [Coverage](coverage-gate.md) |
| TEST-04 | Mutation and flakiness budgets | A | [Mutation](mutation-flakiness.md) |
| SEC-01 | Security and trust-boundary policy | R | [Security](security-gate.md) |
| DEP-01 | Dependency and supply-chain policy | R | [Dependencies](dependency-gate.md) |
| REL-01 | Approved performance and resource budgets | A | [Performance](performance-gate.md) |
| QUAL-01 | Required formatting, lint and type checks | R | [Static quality](static-quality.md) |
| DEL-02 | Authorized requirement completeness | R | [Requirements](requirements-gate.md) |
| DEL-03 | Required documentation and contract consistency | R | [Documentation](documentation-gate.md) |
| DEL-01 | Required build, packaging and release checks | R | [Release](release-gate.md) |
| AI-01 | Agent/tool behavior and permission regression | R | [Agent change](agent-change-gate.md) |

A project may split a rule into specific contract IDs (for example ARCH-01/domain-no-infrastructure). Use the same decision semantics for each. Do not silently repurpose an ID or remove an applicable required rule.
