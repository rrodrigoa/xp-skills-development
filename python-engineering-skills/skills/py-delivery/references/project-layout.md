# Project layout and pyproject

## Use when
New library, tool or service.

## Avoid when
Reorganizing mature package without benefit.

## Implementation
Use src/<package>, tests, docs, pyproject, README, license if owner selects one, CI. Declare build backend, requires-python and dependencies; use existing toolchain.

## Verification and review
Build wheel/sdist, install in clean venv, import and run entry point.
