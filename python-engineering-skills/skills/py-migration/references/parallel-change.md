# Expand, migrate, contract

## When to load
Changing a public interface or persistent schema with independent consumers.

## Procedure
Expand compatibly, identify old/new producers and consumers, migrate with observable progress, then contract only after supported consumers and rollout window permit. Specify version compatibility, defaults and recovery after partial deployment.

## Required evidence and acceptance
Compatibility matrix across versions, migration counts or evidence, rollback limitations and approval for removal.

## Guardrails
Do not assume all consumers upgrade atomically. Reversal may be impossible after data loss; require explicit plan.
