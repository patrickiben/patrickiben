### Patrick Iben, MS · Clinical biostatistics, AI evaluation, and applied mathematics

I build statistical methods and reproducible validation tools for clinical research and AI systems. My work asks whether a claimed signal is actually there, and reports honestly when it is not.

7 years of clinical biostatistics at a CRO (early-phase clinical pharmacology, CDISC/ADaM, PK/NCA) and 12 years in research. Open to research-scientist, AI-evaluation, model-validation, and methods roles. Remote US.

**Contact:** patrickiben@gmail.com · ORCID [0009-0005-2443-7973](https://orcid.org/0009-0005-2443-7973)

#### Featured case study: research engineering and systems architecture

**[Coastal Water Resilience — explore the live console](https://patrickiben.github.io/public-data-consoles/consoles/coastal-water-resilience/)**

I translate mathematical research into interactive decision-support systems. This console brings spatial exposure and spillover diagnostics from my [CRT design framework](https://github.com/patrickiben/crt-design-demo) together with directed source/sink accounting from my [network-contagion research](https://github.com/patrickiben/directed-asymmetry-contagion). It connects live NOAA/NWS feeds, a synthetic lift-station network, scenario controls, and metric-to-response explanations, with explicit labels for measured and modeled information. The public demonstration uses a synthetic network and descriptive scenarios.

#### Selected work

- **[Clinical biostatistics and AI portfolio](https://github.com/patrickiben/biometrics-ai-portfolio)** — SAS and R TLF pseudocode libraries, a synthetic ADaM generator, study-lifecycle tools, and a runnable validation harness. Public and synthetic data; templates and prototypes are labeled.
- **[eCRF pipeline apps](https://github.com/patrickiben/ecrf-pipeline-apps)** · [demo overview](https://patrickiben.github.io/ecrf-pipeline-apps/) — Four Streamlit apps for coding assistance, PII/PHI redaction, participant risk scoring, and anomaly/drift checks. Hosted demos use bundled synthetic data and placeholder dictionary codes; runnable QC checks accompany the source.
- **[numguard](https://github.com/patrickiben/numguard)** — Deterministic checks of extracted numeric values against allowed facts, required facts, and a finite phrase denylist; JSON/JUnit export for CI. A grounding prototype with explicit limits, not validated regulatory software.
- **[calibrated-clinical-ml](https://github.com/patrickiben/calibrated-clinical-ml)** — From-scratch calibration and decision-curve evaluation against a synthetic oracle; demonstrates how identical AUC can conceal different probability calibration.

#### Research

- **Contamination-resilient cluster randomized trial design under spatial interference: a simulation study of contamination control.** *Statistics in Medicine* (submitted). Preprint: [doi:10.5281/zenodo.23486177](https://doi.org/10.5281/zenodo.23486177). Code and data: [doi:10.17605/OSF.IO/XPA4S](https://doi.org/10.17605/OSF.IO/XPA4S). Live demo: [crt-design-demo](https://patrickiben.github.io/crt-design-demo/)
- **What do within-site comparisons of AlphaGenome Atlas predictions measure? An audit at ClinVar sites in 11 genes.** *Human Genomics* (submitted). Preprint: [doi:10.5281/zenodo.23543155](https://doi.org/10.5281/zenodo.23543155). Code and data: [doi:10.5281/zenodo.23537469](https://doi.org/10.5281/zenodo.23537469). Demo: [alphagenome-allele-demo](https://patrickiben.github.io/alphagenome-allele-demo/)
- **A False Floor: Refuting Our Own Information-Limit Claim in a Lethal Identification Task.** Submitted to PLOS ONE, 22 October 2026. Preprint: [doi:10.5281/zenodo.23578222](https://doi.org/10.5281/zenodo.23578222). Records: [doi:10.5281/zenodo.23569075](https://doi.org/10.5281/zenodo.23569075)
- **Anticipating network contagions: when directedness outperforms connectedness.** *Applied Network Science* (with editor). Code and data: [directed-asymmetry-contagion](https://github.com/patrickiben/directed-asymmetry-contagion)
- **Which data modality recognizes a gene set? A domain-agnostic consilience engine.** *PeerJ* (in peer review). Code: [consilience-engine](https://github.com/patrickiben/consilience-engine)
- **No emotion-specific image-computable code in the human left amygdala.** Peer Community In, preprint review. Preprint: [doi:10.5281/zenodo.21422754](https://doi.org/10.5281/zenodo.21422754). Code: [amygdala-invariance](https://github.com/patrickiben/amygdala-invariance)

#### Additional AI-evaluation tools

Each has a dependency-free core self-test. The HTTP service also requires FastAPI and its dependencies.

- **[tool-grounded-agent](https://github.com/patrickiben/tool-grounded-agent)** — A scripted planner demonstrates tool-ledger provenance and a grounding backstop. The harness includes executable known-gap tests; it does not run a language model.
- **[grounded-rag](https://github.com/patrickiben/grounded-rag)** — Lexical retrieval and an extractive answerer with checks for numeric membership and lexical support. A runnable evaluation prototype.
- **[guarded-llm-service](https://github.com/patrickiben/guarded-llm-service)** — The grounding guard served over FastAPI with Docker, CI, and Prometheus-style metrics.

#### Public-data tools

- **[public-data-consoles](https://github.com/patrickiben/public-data-consoles)** — Browser-based dashboards for hazards, early warning, and public health. Descriptive, not predictive.

<sub>Everything here uses public or synthetic data. Proofs of concept are labeled as such.</sub>
