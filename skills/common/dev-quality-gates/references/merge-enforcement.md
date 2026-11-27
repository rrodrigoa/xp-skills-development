# Merge protection and CI integration guidance

## When to load
Configuring a host to enforce gate decisions.

## Procedure
Map stable required check identities to host protections; restrict who can emit/override them. Ensure results are bound to the reviewed head or merge candidate, refresh after changes, and handle merge queues. Separate untrusted PR execution from trusted status publication, use least privilege and audit overrides.

## Required evidence and acceptance
Document required check source, protected branch, stale result handling, authorization and dry-run validation on failing and passing changes.

## Guardrails
This repository contains no CI config or enforcement code. Do not grant reviewers merge authority merely by loading the skill.
