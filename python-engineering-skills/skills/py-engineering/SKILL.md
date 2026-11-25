---
name: py-engineering
description: "Route Python engineering tasks; apply mandatory quality rules, select minimal references, plan changes and verify results."
---
# Python Engineering

1. Read repository instructions and inspect existing package boundaries, tests, configuration and public APIs. Never replace local conventions without justification.
2. Classify task by intent using the route table. Load the relevant skill and only its matching references. For small changes, avoid architecture work unrelated to the request.
3. For changes involving state, policy, external I/O or multiple callers, explicitly identify owners, collaborators and dependency direction before editing. Prefer a pure function for genuinely stateless operations.
4. Make a small vertical change including implementation and behavioral tests. Reuse existing abstractions first. Maintain compatibility unless the user authorizes a break.
5. Run configured checks; inspect the diff for duplication, boundary leaks, suppressed errors, fabricated results and incomplete work. Report commands, outcomes and unverified gaps. Never claim a gate passed without evidence.

| Task | Start with | Add only if relevant |
|---|---|---|
| New subsystem, domain, service | py-architecture | py-patterns, py-testing |
| Choose or implement a pattern | py-patterns | py-architecture, py-testing |
| Feature, library, API, CLI | py-implementation | py-patterns, py-testing |
| Existing procedural or tangled code | py-refactoring | py-architecture, py-patterns, py-testing |
| Test, regression, coverage | py-testing | py-reliability |
| Build, package, CI, release | py-delivery | py-testing, py-reliability |
| Security, concurrency, performance | py-reliability | py-testing |
| Agents, MCP, LLM tools | py-agent-systems | py-architecture, py-reliability, py-testing |
| Architecture audit, metrics, dependency graphs | py-architecture-analysis | py-architecture, py-quality-gates |
| Pattern migration, generation blueprint, codemod plan | py-migration | py-refactoring, py-patterns |
| Independent PR or release gate | py-quality-gates | py-architecture-analysis, py-testing |
| Policy, agent orchestration, baselines, exceptions | py-governance | py-quality-gates |

Context budget: initially load at most two detailed references; expand only to resolve concrete questions. Do not recursively load directories. Preserve selected paths, decisions and verification state in a compact task note if context is compacted. Never omit a relevant security or verification requirement merely to satisfy this soft budget.

Role boundary: reviewer and gate agents must not edit code or alter thresholds unless explicitly reassigned and independently reviewed. Use approved policy and revision-bound evidence. Missing evidence is not a pass. This repository supplies instructions only; perform authorized work using target-project tools, never expect a bundled runtime.
