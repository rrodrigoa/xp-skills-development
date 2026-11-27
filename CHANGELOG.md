# Release notes

## 1.0.0 — guidance-only consolidated release

This release incorporates the planned v0.2, v0.3, v0.5 and v1.0 deliverables as prose specifications. It deliberately skips v0.4 (evaluation runtime). Existing nine skills and reference topics are retained, with executable examples converted into prose or removed; the repository adds four discoverable skill families.

| Planned milestone | Delivered guidance |
|---|---|
| v0.2 | Architecture inventory, import/call/data graphs, cycle detection, coupling/cohesion/complexity definitions, procedural density, duplication, temporal coupling, API surface, architecture contracts, fitness criteria, drift, semantic grouping and reporting. |
| v0.3 | All 35 pattern-specific migration recipes; mechanical and semantic migration, branch by abstraction, expand/migrate/contract, strangler, rollback, and reusable generation blueprints for libraries, CLI, API, agent tools, plugins and workers. |
| v0.5 | Stable gate IDs, decision protocol, PR scope, evidence, architecture/reuse/complexity/API/test/coverage/security/dependency/performance/release/agent quality, anti-gaming and host integration. |
| v1.0 | Project governance profile, authority, agent roles, workflow and handoffs, risk, versioning, baseline, exceptions, calibration, continuous review, incident feedback, adherence and policy maintenance. |
| v0.4 | Not implemented. Existing evaluation scenarios are retained as prose, not executable tests. |

Breaking packaging change: the v0.1 installer, AST audit tool, examples, tests, runtime configuration, CI workflow and executable scaffolds are removed. Install skills manually and use the new guidance with the target project's authorized tooling. Replace only package-owned files. Existing project policies and approved thresholds must be reviewed, not overwritten.

The term "delivered" means written guidance exists, not that an analyzer, migration generator, gate service or autonomous governance runtime has been implemented.

## v2.0.0 — Shared development and language overlays
Breaking organizational change: moved the former Python package to common and language-specific skill groups. All prior reference topics are represented in the common layer (with language-specific detail in overlays), all 35 pattern recipes remain canonical, and all 18 gate IDs remain stable. Added Java design, implementation, testing, delivery and runtime guidance; expanded Python overlays and mixed-language contracts, policy and evidence. Updated role prompts, catalog, installation and migration guidance. No code or runtime added. See MIGRATION.md for old-to-new names.

## v2.1.0 — Observability and operational engineering
Added four independent common skills for READS, observability, Grafana and alerting. Expanded Python and Java telemetry/runtime and testing overlays; integrated observability into task routing, engineering policy, role prompts, architecture, verification, delivery and governance. Added four OBS gate IDs with original decision semantics, six prose worksheets and new evaluation scenarios. All existing skill names, pattern recipes and original 18 gate IDs remain. No executable implementation, generated config, or runtime included.

## v2.2.0 — Deterministic AI development
Five common skills extend the trust hierarchy, architecture/API constraints, custom rule and fixture engineering, runtime feature maps/drivers, formal verification and controlled agent factories. Add Python/Java overlays, four DET gates, seven worksheets, 14 prose scenarios, a practical adoption walkthrough and talk-to-skill traceability. Preserve all prior files and gate semantics. No code or runtime is bundled; consuming projects implement authorized controls.
