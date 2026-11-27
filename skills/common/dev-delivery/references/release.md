# Versioning and releases

## Use when
Publishing artifact or breaking change.

## Avoid when
Publishing without explicit authorization or mutable release tags.

## Implementation
Use documented version policy, changelog and release notes; build once, verify artifacts, trusted publishing where configured, protected tags and approvals; plan rollback/yank.

## Verification and review
Verify artifact version, hashes and clean install; report publication only if confirmed.

## Monitoring readiness
For an applicable release inspect metric/schema consumer compatibility, mixed-version rollout, telemetry health, READS verification, dashboard and alert readiness, owner and rollback. Apply approved OBS gates; distinguish pre-release staging evidence from deployed smoke checks. See dev-observability migration and dev-alerting testing-rollout.
