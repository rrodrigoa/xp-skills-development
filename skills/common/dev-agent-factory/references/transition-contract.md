# Worked deterministic workflow transition contract

## When to load
Designing or verifying a coding agent graph. Use workflow-graph, node-contracts and the canonical gate decision protocol. Adapt to the target engine; this is a specification, not a runtime.

## State ownership
The host owns task identity, approved requirement/policy revision, base and candidate content digest, active node, authorization, gate applicability, actual evidence receipts, retry counters, deadlines, cancellation and terminal outcome. Model output is a proposal with typed data, not a trusted update to these fields. Each external effect has a scoped capability, stable idempotency key and attributable outcome. Checkpoint atomic state transitions with a version; reject stale writes after resume or competing execution.

| From | To | Guard evaluated by trusted host |
|---|---|---|
| Intake | Inspect | Target and allowed scope resolved, workspace available |
| Inspect | Plan | Baseline and constraints recorded; unavailable inputs explicitly classified |
| Plan | Implement | Acceptance fixed, edits authorized, required human approvals satisfied |
| Implement | Verify | Candidate frozen; diff within authorized scope, no unauthorized policy edit |
| Verify | Gate | All required check attempts have attributable results or explicit missing status; revision matches |
| Verify or Gate | Repair | Known repairable defect, authorization and remaining budget, no policy change required |
| Repair | Verify | New candidate frozen; old affected evidence invalidated; retry count durably updated |
| Gate | Approval | Independent result ELIGIBLE; required external approval outstanding |
| Gate or Approval | Complete | Required evidence current, independent technical eligibility, applicable approvals present; no merge effect implied |
| Any nonterminal | Hold | Missing authority/evidence, ambiguous intent, blocked dependency, exhausted budget |
| Any nonterminal | Cancelled | Cancellation accepted; in-flight effects reconciled and cleanup initiated |

An independent gate reports HOLD for missing required evidence and BLOCK for known required failures; the host may route a known repairable failure to a bounded repair branch. A terminal result records the disposition of all external effects. A separate authorized merge host rechecks candidate/merge-queue revision and applicable approvals. Completion of implementation is not release authority.

## Required negative transition cases
Attempt direct Implement-to-Complete, forged PASS string, failed check with zero wrapper exit, missing required result, stale head, changed policy, unapproved check suppression, duplicate event, concurrent checkpoint write, cancelled run resuming, exhausted repair counter and reviewer acting as author. Each must be rejected or sent to the specified safe state. Exercise ordinary success and independently approved waiver without reporting waiver as PASS. Test actual host guards separately from LLM behavior; record graph definition, state schema, evidence and event versions.

## Guardrails
Transitions may be deterministic while model choices, network timing and external state are not. Use the gate protocol rather than inventing new outcomes. Do not turn the HOLD branch into an automatic bypass or allow a model to edit its own authority.
