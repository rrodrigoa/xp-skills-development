# Agent role model and separation of duties

## When to load
Multiple coding, testing and reviewer agents collaborate.

## Procedure
Assign planner/architect to design, implementer to changes, verifier to tests and evidence, independent evaluator to gate decisions, governance owner to policy and exceptions, host/maintainer to merge. Small projects may combine roles except where independent review is required. Pass compact artifacts, not hidden reasoning.

## Required evidence and acceptance
Role assignment with permitted actions, inputs, outputs and approval checkpoints; independent evidence for high-risk changes.

## Guardrails
Agents cannot promote their own privileges, approve their own exceptions or merge because another agent suggested it.

## Operational roles
Assign service health owner, instrumentation implementer, monitoring asset owner, read-only diagnostic agent, alert/incident responder and independent evaluator. A responder may perform only separately authorized operations; design or diagnosis does not grant deployment, silence or merge authority. Use dev-alerting change-governance and incident-response for action boundaries.
