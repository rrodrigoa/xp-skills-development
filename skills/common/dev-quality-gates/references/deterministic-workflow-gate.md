# Controlled agent workflow and automation gate

## When to load
Agent graph, verification runner, release automation or self-improvement changes.

## Implementation in the target project
Use dev-agent-factory workflow-graph, node-contracts, repair-loop, independent-verifier and controlled-automerge. Verify host-owned transitions, permissions, evidence invalidation, bounded retries, independent roles and protected policy. Test unauthorized merge, stale evidence, cancellation, duplicate trigger and failure routing.

## Required evidence and acceptance
Observed negative transition tests and authorized policy; known bypass FAIL; missing required host evidence UNKNOWN.

## Guardrails
Graph prompts or a self-reported status do not constitute deterministic enforcement. No new merge authority.
