# Java packaging and releases

## Shared guidance
dev-delivery: packaging, release; dev-quality-gates: release-gate

## When to load
Publish library or executable.

## Language-specific decisions
Verify JAR/POM metadata, manifest/launcher, source/Javadoc artifacts when required, dependency declarations, signing/provenance and approved registry. For shaded JARs verify merged service resources, relocation, license notices and duplicate classes. Test target JDK and actual packaging type.

## Verification and evidence
Capture artifact hashes, fresh consumer tests, build reproducibility constraints and release approval.

## Avoid
Shipping test classes or secrets; publishing without authority; assuming fat JAR works because unit tests passed.
