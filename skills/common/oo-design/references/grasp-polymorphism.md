# GRASP Polymorphism and Protected Variations

## When to load
Variants repeatedly force callers to change or a dependency is volatile.

## Design procedure
Identify the stable client need and actual dimension of variation. Put varying behavior behind a narrow contract; choose implementations at composition boundary or deliberately closed dispatch. Protect callers from volatile details through stable interfaces, adapters or data mappings. For closed and stable variants, exhaustive dispatch can be clearer than an open hierarchy. Do not invent a variation point before identifying plausible independent change.

## Verification
Run a shared contract suite for every implementation and check unsupported variants. Demonstrate a representative new variant can be added without modifying unrelated clients, or justify closed dispatch.

## Avoid
Type checks spread across callers, speculative plugin APIs, or inheritance for a closed constant choice.
