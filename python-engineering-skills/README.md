# Python Engineering Skills — v1.0.0

A portable, **Markdown-only** knowledge and governance repository for coding agents, automated implementation agents, architects, test agents, independent reviewers and PR gate evaluators. It provides instructions, decision criteria, design blueprints, role contracts and prose templates. It does not supply source code, scripts, generators, CI configuration, executable tests or a runtime. Target projects provide their own tools and policy approvals.

## Start here

- Interactive coding agent: read the project instructions, then discover `py-engineering` and follow its task router.
- Architecture auditor: select `py-architecture-analysis`; use the approved architecture contracts and report evidence, not just metrics.
- Refactoring or generation agent: select `py-migration`, then the appropriate pattern or blueprint.
- Independent reviewer or automated PR gate: select `py-quality-gates`; begin with decision protocol and gate catalog. No approved policy or missing required evidence means HOLD, not pass.
- Governance maintainer or orchestrator: select `py-governance`; establish project profile, role authority, baselines, exceptions and policy lifecycle.

The [catalog](CATALOG.md) is a human/search index, not default model context. [Role entry prompts](integration/ROLE-PROMPTS.md) can be pasted into a harness without requiring custom software. [Governance templates](templates/README.md) are prose worksheets. The [worked governance walkthrough](integration/GOVERNANCE-WALKTHROUGH.md) illustrates how roles and gates interact. [Release notes](CHANGELOG.md) explain the migration from v0.1.

## Manual installation and upgrades

Copy the individual directories under `skills/` into the agent's supported skill discovery location, preserving each `SKILL.md` and its `references/`. Common project locations are `.claude/skills/` for Claude Code and `.agents/skills/` for Codex; common user locations are `~/.claude/skills/` and `~/.agents/skills/`. Confirm discovery settings for the actual client/version; a generic agent can read selected Markdown directly. Reload the client if necessary. No installation utility is provided.

Merge the appropriate text from `integration/CLAUDE.md` or `integration/AGENTS.md` into the target project's instructions; do not overwrite unrelated instructions. Root `AGENTS.md` and `CLAUDE.md` are for maintaining this guidance repository itself, not direct copies for target projects. Review policy conflicts before adopting. For upgrades from v0.1, back up existing skills, then replace only matching package-owned directories so obsolete executable examples are not retained. Remove old package-owned installer/audit/example files only if no local customizations depend on them; never delete unrelated user material.

## Context discipline

Skill metadata is discoverable; load one task-specific SKILL.md and one or two relevant reference cards initially. Expand as concrete design or verification questions arise. For review, read the gate protocol, catalog and affected rule cards, not every coding guide. Required security and evidence rules take priority over a soft context budget. Preserve loaded paths, policy version, key decisions and evidence references in handoffs. Cross-skill names refer to separately discoverable skills, so each skill can be copied intact without root documents; root templates and scenario prompts are optional supporting material.

## Governance adoption

Use the project-profile card in `py-governance` to define actual package contracts, risk tiers, applicable required gates, evidence sources, approved numeric thresholds and approval roles. The gate catalog recommends defaults but does not automatically impose universal rules. Adopt objective checks in the target project's existing CI or reviewer workflow; this repository does not execute or enforce them. Start with a versioned baseline and advisory calibration, then enable required checks after independent approval. Preserve pure functions where appropriate; do not measure design quality by class counts.

## Repository map

- `skills/`: portable skill entry points and granular prose reference cards.
- `integration/`: target-project policies and role-specific prompts.
- `templates/`: prose worksheets for architecture, migration, gate evaluation and governance.
- `evals/`: prose scenarios and scoring guidance only; no evaluation harness.
- `CATALOG.md`, `SOURCES.md`, `CHANGELOG.md`, `VERIFICATION.md`: discovery, research, scope and package checks.

## Limitations

These are engineering standards and instructions, not a claim that an agent will comply or that a merge is safe. Actual tool execution, CI enforcement, reviewer identity, policy approval, model adherence and target-project outcomes must be verified in the host. No v0.4 runtime is included. No universal Python version, coverage threshold, class quota or architecture is imposed.
