# Python packaging and public distributions

## Use when
Publishing reusable library or CLI.

## Avoid when
Depending on source-tree imports or undeclared files.

## Implementation
Use PEP 517 build, project metadata and console scripts; include required package data and py.typed if typed library. Verify wheel and sdist independently.

## Verification and review
python -m build; inspect artifacts; install wheel and smoke test.
