# Dashboard variables and scope safety

## When to load
Building reusable dashboards across environments or services.

## Procedure
Use bounded variables for datasource, environment, cluster, namespace, service, operation and region as applicable; set safe defaults and dependencies. Use proper datasource-specific escaping and multi-value matching; verify all-selection semantics and empty results. Keep environment/tenant isolation at the datasource authorization layer rather than relying on dropdowns. Avoid high-cardinality variable queries or unrestricted query fan-out; inspect refresh and time-range behavior. Preserve scope and time in links to drilldowns. Alert rules execute independently of dashboard session state; use explicit selectors or multidimensional rule labels instead of interactive template variables.

## Required evidence and acceptance
Test single/multi/all/empty scope, special characters, cross-tenant denial, link context and variable query latency.

## Guardrails
Never treat a dashboard variable as an access control or copy unresolved interactive variables into alert expressions.
