# Adopt deterministic AI development in a target repository

This is an executable-work specification for an authorized coding agent, not a promise that instructions alone enforce anything. Keep this skills repository Markdown-only. Create actual code, tests, scripts, CI, drivers and formal specs in the target repository, using its approved tools and permissions. Never edit unrelated projects or enable auto-merge without explicit authority.

## Phase 0 — Inspect and establish baseline
Load dev-deterministic bootstrap and trust-hierarchy. Record exact base, clean/dirty state, policy, supported build units, toolchain, test discovery, existing commands, architecture boundaries, critical features, repeated mistakes and known failures. Run available checks and collect outputs; do not silently fix inherited failures or install unapproved dependencies. Inventory missing tools and permission blockers. Identify approved representative vertical slice and acceptance criteria. If policy is absent, develop proposals and independently reviewable local implementation as authorized; do not claim authoritative gate pass.

## Phase 1 — Make the correct implementation easy
Pick one repeated or high-impact mistake. Reproduce it. Identify causal ownership, canonical good example and public contract. Use oo-design and oo-patterns to improve the API, types, package boundaries and lifecycle. Retire unsafe examples incrementally; preserve compatibility, and isolate approved low-level exceptions. Add characterization and regression tests. Record the constraint ID and residual risk. Do not create a generic framework when a small API suffices.

## Phase 2 — Make violations fail automatically
Use dev-enforcement rule-contract, check-fixtures and ci-enforcement. Implement a narrow local check using existing toolchain where possible. Create isolated positive, negative, bypass and tool-failure fixtures; run them and demonstrate expected diagnostics and exit status. Define a canonical verification command and integrate with existing CI within authority. Preserve independent policy and baseline controls. Report remote branch protection as unverified unless actually checked. Add no-new-regression baseline only with approval.

## Phase 3 — Let the agent run and verify the product
Use dev-runtime-verification feature-map, runtime-driver and independent-oracles. Map critical features with stable IDs, user-visible states and expected outputs; implement a reusable driver, isolated test setup/reset, semantic locators or API calls, bounded execution and evidence capture. Verify positive and negative journeys against actual candidate and include logs, traces, screenshots/video as appropriate. Check driver failure behavior. Add property tests, fuzz replay, fault and timing tests where risk warrants. No production data or third-party traffic by default.

## Phase 4 — Verify critical properties precisely
Use dev-formal-verification method-selection. Select a high-risk protocol or algorithm only when justified. Review property intent and assumptions, implement TLA+/TLC or Lean/approved alternative in target repository, run checker and preserve bounds, theorem, axioms and counterexamples. Translate model failures into concrete tests; map spec to implementation. If tools unavailable, report gap; never claim proof from generated text. If formal verification is not justified, record why and use appropriate behavioral evidence.

## Phase 5 — Integrate deterministic workflow
Use dev-agent-factory workflow-graph, node-contracts and repair-loop. Where a target orchestration engine exists, implement typed state and host-owned guards around plan, implementation, checks, verification, independent gate and approval. Use existing framework; if no orchestration was requested, implement the canonical local verification path and propose optional automation rather than introducing a new runtime. Make negative transitions fail: stale evidence, missing tests, unauthorized action, exhausted repair, invalid state. Separate author/evaluator/merge authority; require explicit authorization for protected settings.

## Phase 6 — Verify and hand off
Run target-project required checks from clean environment where feasible, confirm actual test discovery, inspect all changed controls, and freeze candidate. Provide independent review and DET gate evidence as applicable. Publish a requirement-to-evidence matrix; distinguish PASS, FAIL, UNKNOWN, WAIVED and NOT_APPLICABLE. Provide actual diff, commands, artifact locations, known limitations, pending approvals, rollout/rollback and prioritized next slices. Never present unexecuted checks as completed.

## Suggested target deliverables (adapt paths to project)
| Deliverable | Acceptance |
|---|---|
| Engineering profile and constraint registry | Owner-reviewed intent, scope, IDs and permissions |
| Canonical APIs and architecture boundaries | Valid use works; prohibited use impossible or rejected |
| Local check and CI entry points | Good/bad fixtures, tool failures, actual execution and protected contexts where approved |
| Regression and property suites | Independent expected results, replayable failures, negative controls |
| Feature map and driver | Real candidate runs, isolation, semantic actions, explicit failure/cleanup |
| Statecharts and runtime evidence | User-visible states match actual behavior, revision-bound artifacts |
| Formal spec/proof where applicable | Actual checker results, scope, assumptions and correspondence |
| Workflow/repair enforcement where requested | Host guards and independent gate, unauthorized transitions rejected |
| READS and factory monitoring where applicable | Correct outcome and failure measurement, no secrets, measurable quality |
| Handoff and evolution backlog | Actual results, limitations, review/approval and next candidate improvements |

## First slice example (language neutral)
An agent repeatedly writes direct persistence calls in a domain service. Establish the approved dependency constraint; reproduce a prohibited import or direct reference. Introduce or reuse a domain-owned persistence interface, migrate one caller, and test public behavior including failure. Implement a structural check that rejects the prohibited dependency and accepts infrastructure implementing the port; test aliases or indirect edges where analyzer supports them. Add fixture execution to canonical local/CI verification. Run the service journey against a test database and assert persisted result and failure semantics; attach telemetry when critical. Independently review compatibility and scope. Only then expand to other services. If a dynamic dependency can evade static analysis, add runtime wiring checks or record residual judgment.

## Paste-ready adoption prompt
Adopt XP Development Skills v2.2.0 in this target repository. Use dev-engineering and dev-deterministic bootstrap first. Implement the above phases incrementally, with the highest-risk recurring defect as the first slice. Inspect actual code and tooling and establish baseline before editing. Create real project-specific architecture constraints, tests, check fixtures, local verification commands and approved CI integration. Build a feature map and reusable runtime verification path for critical features. Use formal methods only for justified properties; implement deterministic graph guards and repair loops if orchestration is in scope. Use independent verification and approved DET gates, preserve original gates, and never change policy or merge authority to obtain success. Return the actual changed files, executed evidence, remaining risks and pending decisions. Do not stop at a written plan when implementation is authorized and feasible. Keep the skills repository guidance-only.
