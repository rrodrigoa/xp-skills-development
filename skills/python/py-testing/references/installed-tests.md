# Python installed artifact and integration tests

## Shared guidance
dev-testing: integration, contract, e2e; dev-quality-gates: test-execution-gate

## When to load
Verify a library or CLI release.

## Language-specific decisions
Test wheel in a clean venv outside source checkout; exercise public imports, package data and console entry point. Test supported Python versions, OS and optional dependency combinations selected by policy.

## Verification and evidence
Capture environment, install result, collected tests, skip reasons and exit status.

## Avoid
Tests accidentally importing source tree or stale editable install.
