# Project engineering governance profile

## When to load
Adopting or upgrading standards for a real project.

## Procedure
Record scope, supported environments, project type, risk tiers, policy version and approvers. Name architecture contracts, public APIs, required/advisory gates, applicability, thresholds, evidence, baselines and waiver authority. Define review/merge roles and existing debt. Start with actual project layout and tools.

## Required evidence and acceptance
Approved versioned profile with every required field in the worksheet below; unresolved choices explicitly marked pending.

## Guardrails
No default Python version, class ratio or coverage floor overrides the project. Pending policy means no authoritative gate pass.

## Profile worksheet (complete in the target project)

| Field | Required content |
|---|---|
| Identity | Project, policy revision, effective date, owner and independent approver |
| Scope | Package roots, services, generated/vendor exclusions, supported Python/OS, release channels |
| Contract | Public APIs, data ownership, dependency rules with stable IDs and applicability |
| Quality | For each gate ID: required/advisory, scope, evidence, approved threshold if numeric, failure behavior |
| Baseline | Revision, method/config version, accepted debt inventory and comparison window |
| Risk | Risk tiers, required check/approval matrix and escalation route |
| Roles | Author, verifier, gate evaluator, waiver approver, status publisher and merge authority |
| Exceptions | Nonwaivable rules, waiver approval and expiry conditions |
| Lifecycle | Review cadence, evidence retention, change approval, policy transition and incident feedback |

Example adoption (illustrative only): a library may require its installed-distribution tests and public API compatibility, while a service may require deployment smoke tests and resource budgets. A project may adopt 90% changed-line coverage after calibration; it is not a universal requirement. Any required rule with an unspecified measurement or threshold must remain UNKNOWN until the policy is clarified.
