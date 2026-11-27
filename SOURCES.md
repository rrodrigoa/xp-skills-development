# Research and standards

Original prose guidance written for this repository. Consult these primary sources and established references when extending the cards; they are not copied into the agent context.

- Agent Skills specification: https://agentskills.io/specification
- Claude skill authoring: https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices
- Claude skills overview: https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview
- OpenAI skill building: https://learn.chatgpt.com/docs/build-skills
- OpenAI eval methodology: https://developers.openai.com/blog/eval-skills
- Gamma, Helm, Johnson, Vlissides, *Design Patterns: Elements of Reusable Object-Oriented Software* (1994), canonical 23 patterns.
- Pattern catalog: https://refactoring.guru/design-patterns/catalog (22 patterns; Interpreter separately included here).
- Percival and Gregory, *Architecture Patterns with Python*: https://www.cosmicpython.com/book/preface.html
- Fowler, *Refactoring*, catalog: https://refactoring.com/catalog/
- PEP 8: https://peps.python.org/pep-0008/ ; PEP 257: https://peps.python.org/pep-0257/
- Protocols: https://typing.python.org/en/latest/spec/protocol.html ; dataclasses: https://docs.python.org/3/library/dataclasses.html
- Python packaging: https://packaging.python.org/en/latest/ ; entry points: https://packaging.python.org/en/latest/specifications/entry-points/
- pytest: https://docs.pytest.org/ ; Hypothesis: https://hypothesis.readthedocs.io/
- Ruff: https://docs.astral.sh/ruff/ ; mypy: https://mypy.readthedocs.io/
- OWASP: https://cheatsheetseries.owasp.org/ ; MCP: https://modelcontextprotocol.io/specification/

## v1.0 research and extensions
- Agent Skills client implementation and progressive disclosure: https://github.com/agentskills/agentskills/blob/main/docs/client-implementation/adding-skills-support.mdx
- Import Linter contracts (external tool documentation): https://import-linter.readthedocs.io/
- Fowler, branch by abstraction: https://martinfowler.com/bliki/BranchByAbstraction.html
- Fowler, parallel change: https://martinfowler.com/bliki/ParallelChange.html
- GitHub protected branches and required checks: https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches
- NIST Secure Software Development Framework SP 800-218: https://csrc.nist.gov/pubs/sp/800/218/final

These are reference reading, not dependencies or claims of certified compliance. Gate semantics, role model, policy IDs and worksheets are original project conventions.

## v2.0 Java and polyglot guidance
- Dev.java language, OO, generics and platform evolution: https://dev.java/learn/ ; https://dev.java/learn/language/oop/ ; https://dev.java/learn/generics/
- Java SE tools (choose documentation matching target JDK): https://docs.oracle.com/en/java/javase/25/docs/specs/man/index.html
- ServiceLoader API (version-specific reference): https://docs.oracle.com/en/java/javase/26/docs/api/java.base/java/util/ServiceLoader.html
- Maven layout and dependency mechanism: https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html ; https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html
- Gradle toolchains and dependency locking: https://docs.gradle.org/current/userguide/toolchains.html ; https://docs.gradle.org/current/userguide/dependency_locking.html
- JUnit documentation: https://docs.junit.org/
- ArchUnit user guide: https://www.archunit.org/userguide/html/000_Index.html
- Additional optional tool references (select approved version): https://site.mockito.org/ ; https://java.testcontainers.org/ ; https://www.jacoco.org/jacoco/ ; https://pitest.org/ ; https://openjdk.org/projects/code-tools/jmh/ ; https://picocli.info/

Tools mentioned are choices for consuming projects, never dependencies of this repository. Do not infer a mandated JDK or tool version from reference URLs.

## v2.1 observability and monitoring research
- Salesforce Engineering, READS service health metrics: https://engineering.salesforce.com/reads-service-health-metrics-1bfa99033adc/
- Google SRE Workbook, monitoring and alerting on SLOs: https://sre.google/workbook/monitoring/ ; https://sre.google/workbook/alerting-on-slos/
- OpenTelemetry concepts, semantic conventions, metric conventions, context, sampling and components: https://opentelemetry.io/docs/concepts/ ; https://opentelemetry.io/docs/specs/semconv/ ; https://opentelemetry.io/docs/specs/semconv/general/metrics/ ; https://opentelemetry.io/docs/concepts/context-propagation/ ; https://opentelemetry.io/docs/concepts/sampling/ ; https://opentelemetry.io/docs/concepts/components/
- OpenTelemetry instrumentation and stability: https://opentelemetry.io/docs/languages/python/instrumentation/ ; https://opentelemetry.io/docs/languages/java/instrumentation/ ; https://opentelemetry.io/docs/specs/otel/versioning-and-stability/ ; https://opentelemetry.io/blog/2025/ai-agent-observability/
- Prometheus instrumentation and histograms: https://prometheus.io/docs/practices/instrumentation/ ; https://prometheus.io/docs/practices/histograms/ ; https://prometheus.io/docs/practices/the_zen/
- Grafana dashboards and provisioning: https://grafana.com/docs/grafana/latest/visualizations/dashboards/build-dashboards/best-practices/ ; https://grafana.com/docs/grafana/latest/administration/provisioning/
- Grafana exemplars, Loki labels and Tempo datasource: https://grafana.com/docs/grafana/latest/fundamentals/exemplars/ ; https://grafana.com/docs/loki/latest/get-started/labels/ ; https://grafana.com/docs/grafana/latest/datasources/tempo/configure-tempo-data-source/
- Grafana alerting best practices and missing data: https://grafana.com/docs/grafana/latest/alerting/guides/best-practices/ ; https://grafana.com/docs/grafana/latest/alerting/guides/missing-data/ ; https://grafana.com/docs/grafana/latest/alerting/fundamentals/alert-rule-evaluation/nodata-and-error-states/
- Grafana SLO best practices: https://grafana.com/docs/plugins/grafana-slo-app/latest/best-practices/

Research consulted 2026-11-25. The READS acronym is attributed to the Salesforce engineering article; the health contracts, OBS gate IDs, worksheets and local review rules are original repository guidance. Select documentation matching the deployed tool/SDK/edition; evolving GenAI conventions require version/stability checks. No external software is bundled.

## Deterministic development and verification (v2.2)
- Lauren Tan, [All Code Is Slop (Except Mine), official talk and transcript](https://ai.engineer/code/2026/talks/lauren-tan); [slide-based article](https://ai.engineer/talks/O_zcc6Xl12g-all-code-is-slop-except-mine); [recording](https://www.youtube.com/watch?v=O_zcc6Xl12g). Primary inspiration; XP adaptations are independent and project-specific.
- [TLA+ overview](https://lamport.azurewebsites.net/tla/high-level-view.html), [TLC documentation](https://docs.tlapl.us/using%3Atlc%3Astart) — model checking, assumptions and temporal properties.
- [Lean language reference](https://lean-lang.org/doc/reference/latest), [validating a proof](https://lean-lang.org/doc/reference/latest/ValidatingProofs/) — theorem scope and axiom audit.
- [Playwright locators](https://playwright.dev/docs/locators), [trace viewer](https://playwright.dev/docs/trace-viewer) — semantic runtime interaction and diagnostics.
- [Hypothesis](https://hypothesis.works/) — property testing and minimized counterexamples.
- [Building Secure and Reliable Systems: code and builds](https://google.github.io/building-secure-and-reliable-systems/raw/ch14.html) — verifiable and hermetic builds.
- [Fuchsia test best practices](https://fuchsia.googlesource.com/fuchsia.git/+/HEAD/docs/contribute/testing/best-practices.md) — hermetic and reproducible tests.
These sources guide tool selection and limitations; verify the target project's actual supported versions and extensions. No external runtime or dependency is imported.
