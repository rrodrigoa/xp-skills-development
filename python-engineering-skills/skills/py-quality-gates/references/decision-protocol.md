# Gate decision protocol

## When to load
Every merge or release evaluation.

## Procedure
Freeze base, head, policy and baseline identity. If an approved policy is absent, report advisory findings and HOLD any authoritative recommendation; do not assign required-rule outcomes from an invented policy. For each applicable required rule record PASS, FAIL, UNKNOWN or WAIVED; use NOT_APPLICABLE only with evidence of scope exclusion. A valid approved exception for a waivable rule is WAIVED, never PASS. GOV-01 and GOV-02 are nonwaivable prerequisites for an authoritative gate decision. Advisory findings do not block unless policy makes them required. Aggregate: BLOCK if any required rule FAILs; otherwise HOLD if any required rule is UNKNOWN, policy missing, evidence stale or approval missing; otherwise ELIGIBLE (with waiver list). Do not publish a passing status unless host authorization explicitly permits it.

## Required evidence and acceptance
Report per-rule applicability, evidence, rule version, outcome, severity, exception and required action; show aggregate and exact revision.

## Guardrails
No average score overrides a hard failure. Missing or skipped checks are UNKNOWN unless proven inapplicable. An eligible recommendation is not a merge action.

## Worked decisions (illustrative, not actual evaluations)

| Observed required outcomes | Recommendation | Reason |
|---|---|---|
| All applicable required rules PASS | ELIGIBLE | All required evidence satisfied, subject to external approval requirements |
| TEST-01 FAIL and ARCH-01 UNKNOWN | BLOCK | Known failure takes precedence; also report unknown |
| TEST-01 PASS on old head only | HOLD | Required current evidence is UNKNOWN |
| ARCH-01 WAIVED by valid exception, all others PASS | ELIGIBLE | Explicitly report waiver; not a clean pass |
| Only advisory concern, all required rules PASS | ELIGIBLE | Advisory findings do not block |
| No approved policy | HOLD | Applicability and thresholds cannot be established |

For unapproved or expired exceptions evaluate the original rule normally. A known prohibited violation is FAIL; insufficient evidence is UNKNOWN. An absent external approval required by policy is HOLD even if technical checks pass. Reevaluate after any new commit or relevant policy change. Never issue actual merge or check status without separate authorization.
