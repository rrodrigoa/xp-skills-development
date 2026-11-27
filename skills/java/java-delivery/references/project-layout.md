# Java project layout and JDK support

## Shared guidance
dev-delivery: project-layout, packaging

## When to load
New module or build layout.

## Language-specific decisions
Follow existing Maven or Gradle conventions: main/test Java and resources, generated output separate. Record JDK build toolchain, compiler release target and runtime support; avoid preview features without explicit approval and deployment flags. Use multi-module builds only for real boundaries.

## Verification and evidence
Build clean checkout, verify toolchain and target runtime, inspect generated outputs and packaged resources.

## Avoid
Changing JDK/build system without compatibility assessment or relying on local IDE setup.
