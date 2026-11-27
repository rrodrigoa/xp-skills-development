# Maven dependency and lifecycle management

## Shared guidance
dev-delivery: dependencies, ci

## When to load
Build Maven project.

## Language-specific decisions
Use checked-in wrapper if present; identify reactor modules, lifecycle phases and profiles. Declare dependencies directly when used, manage versions centrally using dependencyManagement/BOM where appropriate, pin plugins and review transitive scope. Surefire and Failsafe may cover different suites; verify lifecycle reaches required integration tests.

## Verification and evidence
Inspect effective POM, dependency tree, resolved versions and actual unit/integration reports; clean build under approved JDK.

## Avoid
Running only compile or test when integration verify is required; unreviewed snapshots or system-scope paths.
