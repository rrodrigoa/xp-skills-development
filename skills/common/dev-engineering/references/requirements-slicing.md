# Requirements, acceptance and vertical slicing

## When to load
The task is a nontrivial feature, broad refactor or multi-agent change.

## Procedure
Extract observable requirements, constraints and explicit exclusions. Resolve what success means at the public boundary; identify error and authorization cases. Map requirements to acceptance evidence. Inventory existing reusable capabilities before designing. Choose a small vertical slice through the relevant domain, application and adapter layers; identify dependencies and approvals. If a decision is reversible and low risk, record the assumption and proceed. If it changes security, compatibility or policy, obtain authority before activation. Keep a compact trace of requirement, implementation location, test and result.

## Review
Every completed requirement has evidence. Incomplete or blocked requirements are explicitly reported. A plan, placeholder, TODO or mock-only implementation is not completion.
