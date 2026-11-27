# Repeatable development and test environment

## When to load
Inconsistent agent results across machines or CI.

## Implementation in the target project
Inspect toolchain and lockfiles, OS/architecture matrix, external services, locale/timezone, configuration, filesystem paths and fixture provenance. Pin or record versions; use isolated temporary state and test credentials; define supported bootstrap and verify commands. Control clocks, random seeds and dependency responses when applicable. Separate network-dependent checks and record their inputs. Test from clean checkout and installed artifact.

## Required evidence and acceptance
Two clean runs on declared environments yield equivalent required outcomes; retain versions, command, seed, artifact and logs. Document variance and unsupported platforms.

## Guardrails
Hermetic tests and reproducible builds are related but distinct; bit-identical artifacts need their own proof. Avoid claiming all concurrency or network behavior is deterministic.
