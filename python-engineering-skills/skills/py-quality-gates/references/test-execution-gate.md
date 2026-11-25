# Test execution and failure gate

## When to load
Any required suite applies.

## Procedure
Determine suites and configurations from project policy; inspect actual execution against reviewed revision. Check selected/collected test counts, skips, expected failures, retries, exit codes and environment. Verify no failure suppression or false-success wrapper.

## Required evidence and acceptance
Trusted results for all required suites; each skip justified under policy; failures or missing suites classified distinctly.

## Guardrails
A command exit code alone may not prove relevant tests ran. No retry-until-green; no synthetic evidence.
