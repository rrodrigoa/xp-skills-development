# Feature map and user journey inventory

## When to load
Agent must locate or test product behavior.

## Implementation in the target project
Map stable feature ID, user vocabulary, entry point, actor/permissions, prerequisites, navigation/actions, expected observable states, negative outcomes and associated test IDs. Link owning code and reusable driver operation; update map alongside intentional behavior changes. Include service/API/CLI/library journeys, not just GUI. Use concise per-feature cards and index by user intent.

## Required evidence and acceptance
An independent agent can find and exercise a feature without reverse-engineering the UI; route and assertion are verified on actual candidate.

## Guardrails
A sitemap alone is not a test oracle. Do not expose secrets or encode brittle coordinates.
