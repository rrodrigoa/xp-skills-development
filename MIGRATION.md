# v1 to v2 skill migration

Use this mapping when upgrading target-project prompts and installed skills. Back up local customizations. Replace package-owned v1 directories, including names reused for narrower Python overlays. Do not keep old routers active; do not delete unrelated skills. Update any explicitly referenced v1 file paths to common or language overlay paths using the catalog. Gate IDs, status semantics and policy authority are unchanged; reapprove adopted policy changes under the consuming project process.

| v1 skill | Canonical v2 shared skill | Relevant Python overlay |
|---|---|---|
| py-agent-systems | dev-agent-systems | As routed |
| py-architecture | oo-design | py-design |
| py-architecture-analysis | dev-architecture-analysis | py-design |
| py-delivery | dev-delivery | py-delivery |
| py-engineering | dev-engineering | As routed |
| py-governance | dev-governance | As routed |
| py-implementation | dev-implementation | py-implementation |
| py-migration | dev-migration | py-implementation |
| py-patterns | oo-patterns | py-design |
| py-quality-gates | dev-quality-gates | py-testing, py-delivery |
| py-refactoring | dev-refactoring | py-implementation |
| py-reliability | dev-reliability | py-runtime |
| py-testing | dev-testing | py-testing |

The source layout is now `skills/common/`, `skills/python/`, `skills/java/`; copy individual skill directories to the discovery root. Do not copy group README files into the host's skill directories. For Java install common plus Java; for Python common plus Python; for mixed-language repositories install all three groups. Verify discovery in the actual host.

## v2.0 to v2.1
Existing skill names and source paths remain valid. Install the four new common skills and replace package-owned existing skills with their updated versions; merge updated project policies and preserve local customizations. Update adopted guidance revision. OBS-01 through OBS-04 are new optional-for-adoption gate IDs (recommended required when applicable and explicitly approved); existing policy is not automatically changed. Review health contracts, telemetry consumers, monitoring assets and operational permission boundaries before activating checks.

## Upgrade to v2.2.0
Install five new common skills; replace package-owned updated skills and merge project instructions without overriding local policy. Keep existing names and gate IDs. DET-01 through DET-04 require explicit applicability, evidence and authority approval. Use the deterministic adoption guide for real target-project implementation. No runtime or executable configuration is included.
