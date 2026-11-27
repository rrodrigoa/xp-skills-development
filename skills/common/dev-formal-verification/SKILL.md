---
name: dev-formal-verification
description: "Specify invariants, model check distributed and concurrent behavior, prove algorithms and connect formal evidence to real implementation."
---
# Formal verification

Use dev-engineering for routing and dev-governance for approved policy. This is guidance only: implement authorized constraints, checks and tools in the consuming repository. Load one or two matching cards first. Use dev-quality-gates for independent decisions; no self-approval or missing-evidence pass.

## Reference selector
- [Choose the right verification method](references/method-selection.md) — High-risk invariant or complex algorithm.
- [Formal specification and invariant inventory](references/formal-spec.md) — Designing safety-critical state or algorithm.
- [TLA+ and bounded model checking](references/tla-model.md) — Distributed protocol, queue, retry, concurrency or notification flow.
- [Lean algorithm proof and proof hygiene](references/lean-proofs.md) — Mathematical algorithm with precise specification.
- [Connect models and proofs to implementation](references/model-correspondence.md) — Formal result is cited for a production change.
- [Counterexample-driven debugging](references/counterexamples.md) — Model checker, prover or property test finds violation.
- [Concurrency and distributed protocol invariants](references/concurrency-protocols.md) — Locks, leases, workflows, retries and messaging.
- [Formal evidence review and regression](references/proof-gates.md) — Formal result participates in release approval.
- [Worked formal model: retry and duplicate delivery](references/worked-protocol.md) — Modeling idempotency, crash and retries.
