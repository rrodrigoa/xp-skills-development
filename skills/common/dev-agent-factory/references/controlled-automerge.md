# Risk-based automation and merge authority

## When to load
Owner proposes unattended PR integration.

## Implementation in the target project
Require approved risk tiers, protected policy, trusted revision-bound checks, independent evaluation, restricted permissions and rollback. Limit eligible classes of changes, exclude security/policy/infrastructure or other high-impact changes unless separately authorized, and require merge-queue revalidation. Treat every unknown required result as hold. Pilot in observation mode; monitor escapes and disable on regression.

## Required evidence and acceptance
Host-level controls and negative scenarios prove unauthorized, stale, failed or high-risk changes cannot merge; owner explicitly approves activation.

## Guardrails
This skill is guidance, not authorization. Never enable auto-merge or change branch rules without explicit permission.
