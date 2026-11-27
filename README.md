# XP Development Skills — v2.2.0

Language-independent development, OO design and engineering governance with Python and Java overlays for coding agents, architecture agents, test agents, independent reviewers and automated PR gate evaluators. Guidance only: no source code, executable examples, CI workflows, generators, installation scripts or evaluation runtime. The target project supplies tools and approvals.

## Layout and ownership

- [Common skills](skills/common/README.md): shared design decisions, all 35 patterns, testing, refactoring, reliability, architecture analysis, delivery, agent systems, gates and governance. Canonical intent and acceptance criteria live here.
- [Python skills](skills/python/README.md): Python-specific types, idioms, tools, runtime and evidence.
- [Java skills](skills/java/README.md): Java-specific types, idioms, JVM, build systems, frameworks and evidence.
- [Catalog](CATALOG.md): search index, not mandatory agent context.
- [Integration](integration/ROLE-PROMPTS.md): role prompts and target-project policies. [Templates](templates/README.md) are prose worksheets; [evals](evals/README.md) are prose scenarios.
- [Migration map](MIGRATION.md), [changelog](CHANGELOG.md), [sources](SOURCES.md), [verification](VERIFICATION.md).

## Manual installation

Copy the **individual skill directories** (the directories containing SKILL.md), not the common/python/java parent folders, into the same agent discovery root. Always install common; add Python, Java or both as appropriate. Typical project roots: `.claude/skills/` (Claude Code) and `.agents/skills/` (Codex); typical user roots: `~/.claude/skills/` and `~/.agents/skills/`. Check actual client discovery and reload as needed. The skill names are unique across groups; internal relative links stay within a skill. Cross-skill references use logical skill identifiers, so flattened installations work without the source repository. A generic agent may instead read selected files from the source tree.

Merge the target-project policy from `integration/AGENTS.md` or `integration/CLAUDE.md` into existing instructions, not over them. Upgrade from v1 by backing up the old package-owned skills and replacing those directories using the migration map; remove stale v1 entries even when names are unchanged. Preserve unrelated skills and local changes. Do not install two conflicting versions of a skill or leave the old py-* routers active. Pin the adopted guidance revision in the target project's engineering profile.

## Routing

Read `dev-engineering` first for nontrivial work. Determine the affected language and build unit, select the shared skill for task intent, then one language overlay only if required. Start with one or two relevant cards; expand when needed for security, correctness or evidence. A Java Strategy decision uses `oo-patterns` strategy plus `java-design` behavioral-patterns; Python uses the same strategy plus `py-design` behavioral-patterns. A Java CLI uses `dev-implementation` cli-design plus `java-implementation` cli. A Python CLI uses the same shared card plus its Python counterpart. Mixed-language boundaries use `dev-implementation` cross-language-contracts and per-component checks. Do not load the entire catalog or both overlays for a single-language task.

## Governance

Use `dev-governance` project-profile to establish approved policy, risk, roles, exact revision, per-component runtime versions, evidence sources and gate requirements. `dev-quality-gates` owns 26 gate IDs (22 preserved plus four deterministic-development gates), outcomes and aggregation; language overlays describe how to collect and interpret evidence, not independent gates. A required missing/stale check is UNKNOWN and prevents eligibility. No self-approval, unapproved threshold changes, class quotas, or automatic merge authority. No runtime, tool execution or enforcement is bundled. Actual host discovery, adherence and target-project checks must be verified independently.

## Observability and monitoring
The common layer includes four separate skills: [dev-reads](skills/common/dev-reads/SKILL.md) (health model and SLI/SLO), [dev-observability](skills/common/dev-observability/SKILL.md) (implementation, telemetry and diagnosis), [dev-grafana](skills/common/dev-grafana/SKILL.md) (dashboards, datasource queries and monitoring assets), and [dev-alerting](skills/common/dev-alerting/SKILL.md) (conditions, routing, incident response and quality). Start with the task intent; never load all references by default. Python/Java runtime and testing overlays contain language-specific telemetry cards.

For feature development, use a READS contract and instrumentation plan where operation risk warrants it. For monitoring, use scoped read-only evidence before proposing a change. For production writes or mitigation require explicit authority. OBS-01 through OBS-04 extend the canonical gate catalog; the consuming project must approve applicability and evidence before they become mandatory. No tools, dashboard JSON, PromQL implementations, configuration, runtime or evaluation harness is bundled. Use the [observability adoption guide](integration/OBSERVABILITY-ADOPTION.md) and selected [worksheets](templates/README.md).

## Deterministic AI development
Five common skills teach agents to implement enforceable engineering in their own repositories: [dev-deterministic](skills/common/dev-deterministic/SKILL.md), [dev-enforcement](skills/common/dev-enforcement/SKILL.md), [dev-runtime-verification](skills/common/dev-runtime-verification/SKILL.md), [dev-formal-verification](skills/common/dev-formal-verification/SKILL.md) and [dev-agent-factory](skills/common/dev-agent-factory/SKILL.md). Start with [target-project adoption](integration/DETERMINISTIC-ADOPTION.md) and [presentation traceability](integration/TALK-TO-SKILLS.md). Implement actual checks, fixtures, drivers and orchestration only in the target project within authority. DET-01 through DET-04 are recommended for explicit policy adoption; existing gate semantics remain. Skills do not themselves enforce checks, provide a runtime or authorize automation.
