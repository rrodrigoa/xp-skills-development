# Worked governance walkthrough (illustrative only)

A team maintains a legacy analytics library and is adding a second data provider. Existing procedural functions share mutable context, and one domain package imports a concrete storage adapter. The following is a hypothetical adoption, not evidence from a real repository.

## 1. Establish the policy
The owner approves a project profile, including API-01, TEST-01, TEST-02, QUAL-01, GOV-01, GOV-02 and a scoped ARCH-01 contract. The architecture contract forbids new domain-to-concrete-storage dependencies, with edge scope and exceptions defined. The preexisting import is recorded as tolerated inherited debt only if policy permits. No coverage or complexity threshold is invented.

## 2. Audit and plan
The architect uses dev-architecture-analysis to identify shared mutation sites and relevant import edges. The implementer chooses an injected consumer-owned storage port and provider adapters, rather than moving functions into static methods. The migration plan preserves the existing API and test behavior, creates shared provider contract tests and retires the old import only after callers move.

## 3. Implement and verify
The coding agent works in the target project, not this guidance repository. A verifier checks the exact candidate: existing compatibility cases, shared provider contract, missing-provider failure, data isolation and configured static checks. Evidence records contain actual revision, configuration and outcomes, not author assertions.

## 4. Independent gate
If a new prohibited import exists, ARCH-01 is FAIL and the recommendation is BLOCK. If only old-revision test evidence is available, TEST-01 is UNKNOWN and the recommendation is HOLD unless an applicable required rule already fails. If the old debt is unchanged and the approved regression rule permits it, that alone does not block; explicitly report the inherited item. If all applicable required rules pass and approvals are present, the recommendation is ELIGIBLE, not an actual merge.

## 5. Ongoing governance
A later review may strengthen the contract to prohibit all such edges after the legacy import is removed. The owner approves the baseline and policy transition; a candidate cannot rewrite its own baseline to avoid a violation. If a waiver is needed, use independent approval, precise scope, verified compensating controls and expiry; the gate reports WAIVED rather than PASS.

Use only the selected skill cards and the relevant prose worksheets at each stage. These steps require the target agent or CI host to collect evidence and enforce decisions; no executable governance service is provided.
