# Gradle toolchains and dependency management

## Shared guidance
dev-delivery: dependencies, ci

## When to load
Build Gradle Java project.

## Language-specific decisions
Use project's Gradle wrapper and configured toolchains. Distinguish api and implementation exposure for Java libraries; use version constraints/catalogs and lock/verification mechanisms per policy. Review task graph and custom integration test source sets; avoid relying on machine caches.

## Verification and evidence
Inspect dependency insight, resolved versions, lock state and actual executed tasks; verify clean build.

## Avoid
Running a task that excludes required suites or changing lock files to hide dependency drift.
