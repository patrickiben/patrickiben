### Patrick Iben, MS · Applied mathematics, research engineering, and clinical biostatistics

I build mathematical frameworks and turn uncertain signals into inspectable, tested systems across clinical biometrics, AI evaluation, wearable sensing, and public-data monitoring.

7 years of clinical biostatistics at a CRO (early-phase clinical pharmacology, CDISC/ADaM, PK/NCA) and 12 years in research. Open to research-scientist, research-engineering, AI-evaluation, model-validation, and methods roles. Remote US.

**Contact:** patrickiben@gmail.com · ORCID [0009-0005-2443-7973](https://orcid.org/0009-0005-2443-7973)

#### Selected work

**Research engineering and systems architecture** — translating methods across domains, integrating data and models, and building tools whose assumptions and evidence can be inspected.

- **[Coastal Water Resilience](https://patrickiben.github.io/public-data-consoles/consoles/coastal-water-resilience/)** · [source](https://github.com/patrickiben/public-data-consoles/tree/main/consoles/coastal-water-resilience) — Spatial exposure and spillover diagnostics from my [CRT framework](https://github.com/patrickiben/crt-design-demo), directed source/sink accounting informed by my [network-contagion research](https://github.com/patrickiben/directed-asymmetry-contagion), and live NOAA/NWS feeds in one infrastructure console. Ten-parameter response plans connect diagnostics to practical next steps. A separate official public-station register and explicit projected-impact exercises complement the synthetic calibration network; observations and assumptions carry separate labels.
- **[Autonomic Telemetry](https://patrickiben.github.io/autonomic-telemetry/)** · [source](https://github.com/patrickiben/autonomic-telemetry) — A local wearable-to-browser research system: Bluetooth adapters, an in-memory Mac bridge, and mobile visualization, with explicit signal quality, freshness, and source contracts. A separate Signal Lab provides numerical lenses with analytic and regression checks.
- **[Resilience Telemetry](https://patrickiben.github.io/public-data-consoles/consoles/resilience-telemetry/)** · [research guide](https://patrickiben.github.io/public-data-consoles/consoles/resilience-telemetry/wiki.html#s8b) — An interactive companion to my [directed-contagion research](https://github.com/patrickiben/directed-asymmetry-contagion): cross-asset spillover analysis, transmitter stability, and baseline comparisons, with public-data ingestion, historical replay, and explicit interpretation limits.

**Clinical biometrics and AI evaluation**

- **[Clinical biostatistics and AI portfolio](https://patrickiben.github.io/biometrics-ai-portfolio/)** · [source](https://github.com/patrickiben/biometrics-ai-portfolio) — SAS and R TLF pseudocode libraries, a synthetic ADaM generator, study-lifecycle tools, and a runnable validation harness. Public and synthetic data; templates and prototypes are labeled.
- **[eCRF pipeline apps](https://github.com/patrickiben/ecrf-pipeline-apps)** · [demo overview](https://patrickiben.github.io/ecrf-pipeline-apps/) — Four Streamlit apps for coding assistance, PII/PHI redaction, participant risk scoring, and anomaly/drift checks. Hosted demos use bundled synthetic data and placeholder dictionary codes; runnable QC checks accompany the source.
- **[numguard](https://github.com/patrickiben/numguard)** — Deterministic checks of extracted numeric values against allowed facts, required facts, and a finite phrase denylist; JSON/JUnit export for CI. A grounding prototype with explicit limits.
- **[calibrated-clinical-ml](https://github.com/patrickiben/calibrated-clinical-ml)** — From-scratch calibration and decision-curve evaluation against a synthetic oracle; demonstrates how identical AUC can conceal different probability calibration.

#### Research

[Manuscript → code → demo map](RESEARCH_MAP.md) — direct draft links, archived releases, and related applications for each study. Submission and review statuses below are current as of 23 October 2026.

- **Contamination-resilient cluster randomized trial design under spatial interference: a simulation study of contamination control.** *Statistics in Medicine* (submitted). Preprint: [doi:10.5281/zenodo.23486177](https://doi.org/10.5281/zenodo.23486177). Code and data: [doi:10.17605/OSF.IO/XPA4S](https://doi.org/10.17605/OSF.IO/XPA4S). Live demo: [crt-design-demo](https://patrickiben.github.io/crt-design-demo/)
- **What do within-site comparisons of AlphaGenome Atlas predictions measure? An audit at ClinVar sites in 11 genes.** *Human Genomics* (submitted). Preprint: [doi:10.5281/zenodo.23543155](https://doi.org/10.5281/zenodo.23543155). Code and data: [doi:10.5281/zenodo.23537469](https://doi.org/10.5281/zenodo.23537469). Demo: [alphagenome-allele-demo](https://patrickiben.github.io/alphagenome-allele-demo/)
- **A False Floor: Refuting Our Own Information-Limit Claim in a Lethal Identification Task.** Submitted to PLOS ONE, 22 October 2026. Preprint: [doi:10.5281/zenodo.23578222](https://doi.org/10.5281/zenodo.23578222). Records: [doi:10.5281/zenodo.23569075](https://doi.org/10.5281/zenodo.23569075)
- **Anticipating network contagions: when directedness outperforms connectedness.** *Applied Network Science* (with editor). Author draft: [PDF](https://github.com/patrickiben/directed-asymmetry-contagion/blob/main/manuscript/anticipating_network_contagions_draft.pdf). Code and data: [directed-asymmetry-contagion](https://github.com/patrickiben/directed-asymmetry-contagion). Related application: [Resilience Telemetry](https://patrickiben.github.io/public-data-consoles/consoles/resilience-telemetry/)
- **Which data modality recognizes a gene set? A domain-agnostic consilience engine.** *PeerJ* (in peer review). Author draft: [PDF](https://github.com/patrickiben/consilience-engine/blob/main/manuscript/consilience_PeerJ_draft.pdf). Code: [consilience-engine](https://github.com/patrickiben/consilience-engine)
- **No emotion-specific image-computable code in the human left amygdala.** Peer Community In, preprint review. Preprint: [doi:10.5281/zenodo.21422754](https://doi.org/10.5281/zenodo.21422754). Code: [amygdala-invariance](https://github.com/patrickiben/amygdala-invariance)

#### Additional AI-evaluation tools

Each has a dependency-free core self-test. The HTTP service also requires FastAPI and its dependencies.

- **[tool-grounded-agent](https://github.com/patrickiben/tool-grounded-agent)** — A scripted planner demonstrates tool-ledger provenance and a grounding backstop. The harness includes executable known-gap tests; it does not run a language model.
- **[grounded-rag](https://github.com/patrickiben/grounded-rag)** — Lexical retrieval and an extractive answerer with checks for numeric membership and lexical support. A runnable evaluation prototype.
- **[guarded-llm-service](https://github.com/patrickiben/guarded-llm-service)** — The grounding guard served over FastAPI with Docker, CI, and Prometheus-style metrics.

#### Public-data tools

- **[public-data-consoles](https://github.com/patrickiben/public-data-consoles)** — Browser-based dashboards for hazards, early warning, and public health. Descriptive, not predictive.

<sub>Shared examples and hosted demonstrations use public or synthetic data. Autonomic Telemetry also supports private local wearable input; proof-of-concept boundaries are documented.</sub>
