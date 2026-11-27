# Presentation-to-skill traceability

Source: Lauren Tan, All Code Is Slop (Except Mine), AI Engineer CODE 2026. [Official talk page and transcript](https://ai.engineer/code/2026/talks/lauren-tan), [official slide-based article](https://ai.engineer/talks/O_zcc6Xl12g-all-code-is-slop-except-mine), [video](https://www.youtube.com/watch?v=O_zcc6Xl12g). Video chapters below are clip-relative. The transcript is machine-generated; use the original recording to resolve uncertain details. These are original engineering adaptations, not a transcript or copied slides.

| Clip topic | XP implementation guidance |
|---|---|
| 2:03 trust hierarchy | dev-deterministic trust-hierarchy; constraints before prose |
| 5:00 framework boundaries | dev-enforcement architecture-framework and architecture-fitness; package ownership, typed APIs |
| 6:56 recurring review comments | dev-deterministic correction-loop, code-as-memory and workaround-removal; tested lint diagnostics |
| 9:40 runtime verification | dev-runtime-verification feature-map, runtime-driver, proof-artifacts and ui-verification |
| 10:50 formal and UI testing | dev-formal-verification tla-model, lean-proofs and model-correspondence; runtime property-fuzz |
| 11:51 verification effort | dev-deterministic verification-budget; statecharts and independent oracles |
| 13:32 throughput and quality | dev-agent-factory factory-observability; measure outcomes, not PR count alone |
| 15:11 foundations before factory | dev-agent-factory workflow-graph, release-fuzzing, parallel-work and controlled-automerge |

XP extensions beyond the talk: explicit gate outcomes, protected checker fixtures and provenance, language overlays, risk-based adoption, evidence invalidation, permission boundaries, bounded retries, failure replay, self-improvement governance and READS monitoring. These are design choices of this repository, not attributed claims. Reported team outcomes are not a guarantee or a target for adopters. The talk's strict local policies about comments and framework APIs are context-specific, not universal bans. Formal checks must be scoped to actual models and proofs. Unattended merging requires a separate explicit project authorization.
