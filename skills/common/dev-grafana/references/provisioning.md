# Grafana dashboard and datasource lifecycle

## When to load
Creating or changing monitoring assets as managed artifacts.

## Procedure
Inspect actual Grafana deployment, version, organization, folder, datasource UIDs, permissions and current management mechanism (file provisioning, approved API, Terraform/GitOps or manual workflow). Choose existing source of truth; maintain stable dashboard UID and datasource references across environments. Record owner, version, query definitions, review and rollback. Do not embed secrets or assume UI edits persist in provisioned assets; understand update/deletion semantics. Preview/import in staging, compare existing assets, validate schema against installed version and preserve unrelated dashboards. For a write require explicit scope and authorization, use read-before-write, conflict protection and diff; never mass overwrite.

## Required evidence and acceptance
Export or snapshot current state, review candidate diff, verify staging datasource/panels/links/permissions and documented rollback; capture actual deployed UID/version if authorized.

## Guardrails
Do not invent dashboards in production, use admin credentials by default or overwrite managed assets outside their source of truth.
