# Repository deterministic-development bootstrap

## When to load
Asked to make an existing repo deterministic.

## Implementation in the target project
Inventory manifests, build roots, dependency graph, public API, tests, CI, available runtime drivers, policy, permissions and supported environments. Run existing checks before edits; classify failures as inherited, newly observed or unknown. Identify the most repeated mistakes from source, PRs, incidents and workarounds; select one representative vertical slice. Produce an adoption plan and target artifacts; obtain approval for new required checks and tool dependencies. Implement constraint, checker, fixtures and runtime verification in that slice; then expand by risk. Preserve baseline and current behavior unless change is approved.

## Required evidence and acceptance
Deliver actual target-repo files, exact commands and observed results for good/bad fixtures, feature execution and independent gate review. Report untouched scope, pending approvals and tool blockers.

## Guardrails
Do not merely add AGENTS.md or claim implementation from a plan. Do not silently replace working build/test pipelines.
