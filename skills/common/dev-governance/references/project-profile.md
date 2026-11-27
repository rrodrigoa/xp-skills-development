# Project engineering governance profile

## When to load
Adopting or upgrading standards for a real project.

## Procedure
Record scope, supported environments, project type, risk tiers, policy version and approvers. Name architecture contracts, public APIs, required/advisory gates, applicability, thresholds, evidence, baselines and waiver authority. Define review/merge roles and existing debt. Start with actual project layout and tools.

## Required evidence and acceptance
Approved versioned profile with every required field in the worksheet below; unresolved choices explicitly marked pending.

## Guardrails
No default language version, class ratio or coverage floor overrides the project. Pending policy means no authoritative gate pass.

## Profile worksheet (complete in the target project)

| Field | Required content |
|---|---|
| Identity | Project, policy revision, effective date, owner and independent approver |
| Scope | Package roots, services, generated/vendor exclusions, supported language/runtime/OS, release channels |
| Contract | Public APIs, data ownership, dependency rules with stable IDs and applicability |
| Quality | For each gate ID: required/advisory, scope, evidence, approved threshold if numeric, failure behavior |
| Baseline | Revision, method/config version, accepted debt inventory and comparison window |
| Risk | Risk tiers, required check/approval matrix and escalation route |
| Roles | Author, verifier, gate evaluator, waiver approver, status publisher and merge authority |
| Exceptions | Nonwaivable rules, waiver approval and expiry conditions |
| Lifecycle | Review cadence, evidence retention, change approval, policy transition and incident feedback |

Example adoption (illustrative only): a library may require its installed-distribution tests and public API compatibility, while a service may require deployment smoke tests and resource budgets. A project may adopt 90% changed-line coverage after calibration; it is not a universal requirement. Any required rule with an unspecified measurement or threshold must remain UNKNOWN until the policy is clarified.

## Multi-language scope
Record each component's language, supported version, build root, dependency resolver, test runner, artifact form, source/generated boundaries and owner. Map shared gate IDs to per-component evidence producers and thresholds. Specify cross-language contracts (wire schema, units, errors, ordering, compatibility), ownership and test matrix. A missing language profile for required evidence remains unresolved; do not silently inherit another language's tool settings.

## Observability profile
For each production component record critical journeys, READS contract/version, SLI/SLO owner and policy, telemetry provider/schema, retention/privacy/access, cardinality and overhead budgets, monitoring assets/source of truth, approved backend/query scopes, alert owner/routes/maintenance and escalation, deployment evidence and independent monitoring-chain coverage. Define operational roles, read versus write authority, approval for production changes, recovery evidence and incident feedback. Adopt OBS-01 through OBS-04 explicitly by component/risk/evidence; no default target or gate is automatically required. Use dev-reads, dev-observability, dev-grafana and dev-alerting for detailed guidance.

## Deterministic development profile
For each component record canonical build/check/start/reset commands, supported environment, requirement/feature IDs, constraint registry, checker owner/version, positive/negative control fixtures, baseline, evidence provenance and retention. Define runtime driver and artifact access, formal property scope and assumptions where justified, approved DET gates and required checks, verification budget, graph transition owner, retry/stop rules and independent approval. Record automation scope, excluded risk classes, rollback and disable authority. No activation by default; project owner approves changes to policy, required contexts and merge permissions.
