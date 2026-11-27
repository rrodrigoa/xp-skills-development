# Python project layout and pyproject

## Shared guidance
dev-delivery: project-layout, packaging

## When to load
New or reorganized Python package.

## Language-specific decisions
Follow pyproject.toml metadata, approved build backend and requires-python. Use src layout when appropriate; declare runtime vs development dependencies, package data and py.typed for typed distributions.

## Verification and evidence
Build wheel and sdist independently, inspect contents and install from each supported artifact.

## Avoid
Unapproved backend migration or depending on source checkout imports.
