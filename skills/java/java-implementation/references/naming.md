# Java naming and package conventions

## Shared guidance
dev-implementation: naming, module-design

## When to load
Name new types, members or packages.

## Language-specific decisions
Follow approved project style: UpperCamelCase types, lowerCamelCase methods/fields, lowercase reverse-domain packages, uppercase underscore compile-time constants. Choose domain terms, verbs for behavior and clear boolean predicates. Use consistent acronym handling and explicit units; respect JavaBeans conventions only where framework contracts require them.

## Verification and evidence
Review exported API, file/type naming, package ownership and binary/source compatibility.

## Avoid
Generic Manager/Utils dumping grounds; treating every final reference as a constant.
