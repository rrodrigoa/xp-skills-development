---
name: py-agent-systems
description: "Design production Python AI agents, MCP tools, LLM adapters, structured outputs, workflow state, safety and evaluation."
---
# Python Agent Systems

Treat model output, tool payloads and external content as untrusted. Keep deterministic orchestration and typed contracts outside the model. Separate provider adapters from workflow and policy. Use bounded tool budgets, explicit authorization and schema validation. Record reproducible eval scenarios and trace outcomes without leaking secrets. Never let a prompt alone enforce permissions.

## Reference selector
Read only relevant files from this list.

- [LLM provider adapter](references/llm-adapters.md) — Multiple OpenAI-compatible or other LLM endpoints.
- [Agent workflow state and orchestration](references/agent-workflow.md) — Multi-step graph, tools and resumable runs.
- [MCP tools and schemas](references/mcp-tools.md) — Exposing reusable tools to agents.
- [Structured model output](references/structured-output.md) — Model emits tool args, plans or JSON.
- [Agent permissions and prompt injection](references/agent-security.md) — Agent handles external content or performs actions.
- [Agent evaluations and regression gates](references/agent-eval.md) — Prompts, models or tools change.
- [Agent tracing and cost budgets](references/agent-observability.md) — Agent execution spans multiple LLMs/tools.
- [Context and skill loading](references/agent-context.md) — Large repositories and constrained local models.
- [Agent-generated code and artifact integrity](references/agent-artifacts.md) — Agent writes code, patches or packages.

For role separation, handoffs and governance of coding/review agents, use `py-governance`; for independent agent change review use `py-quality-gates`.
