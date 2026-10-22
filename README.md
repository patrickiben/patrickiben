### Patrick Iben, MS: applied mathematician

I build mathematical frameworks and validation pipelines for biometrics, generative AI, and complex dynamical systems. Most of what's here asks whether a claimed signal is actually there, and reports honestly when it isn't.

7 years of clinical biostatistics at a CRO (early-phase clinical pharmacology, CDISC/ADaM, PK/NCA) and 12 years in research. Open to research-scientist, AI-evaluation, model-validation, and methods roles. Remote US.

**Contact:** patrickiben@gmail.com · ORCID [0009-0005-2443-7973](https://orcid.org/0009-0005-2443-7973)

---

#### Research

- **Contamination-resilient cluster randomized trial design under spatial interference: a simulation study of contamination control.** *Statistics in Medicine* (submitted). Preprint: [doi:10.5281/zenodo.23486177](https://doi.org/10.5281/zenodo.23486177). Code and data: [doi:10.17605/OSF.IO/XPA4S](https://doi.org/10.17605/OSF.IO/XPA4S). Live demo: [crt-design-demo](https://patrickiben.github.io/crt-design-demo/)
- **What do within-site comparisons of AlphaGenome Atlas predictions measure? An audit at ClinVar sites in 11 genes.** *Human Genomics* (submitted). Preprint: [doi:10.5281/zenodo.23543155](https://doi.org/10.5281/zenodo.23543155). Code and data: [doi:10.5281/zenodo.23537469](https://doi.org/10.5281/zenodo.23537469). Demo: [alphagenome-allele-demo](https://patrickiben.github.io/alphagenome-allele-demo/)
- **A False Floor: Refuting Our Own Information-Limit Claim in a Lethal Identification Task.** Submitted to PLOS ONE, 22 October 2026. Preprint: [doi:10.5281/zenodo.23519300](https://doi.org/10.5281/zenodo.23519300). Records: [doi:10.5281/zenodo.23569075](https://doi.org/10.5281/zenodo.23569075)
- **Anticipating network contagions: when directedness outperforms connectedness.** *Applied Network Science* (with editor). Code and data: [directed-asymmetry-contagion](https://github.com/patrickiben/directed-asymmetry-contagion)
- **Which data modality recognizes a gene set? A domain-agnostic consilience engine.** *PeerJ* (in peer review). Code: [consilience-engine](https://github.com/patrickiben/consilience-engine)
- **No emotion-specific image-computable code in the human left amygdala.** Peer Community In, preprint review. Preprint: [doi:10.5281/zenodo.21422754](https://doi.org/10.5281/zenodo.21422754). Code: [amygdala-invariance](https://github.com/patrickiben/amygdala-invariance)

#### Trustworthy-AI tooling

All zero-dependency, all with runnable self-tests.

- **[numguard](https://github.com/patrickiben/numguard)**: a guardrail and evaluation harness for LLM output in regulated work. The model never sources a number; JSON/JUnit export for CI.
- **[tool-grounded-agent](https://github.com/patrickiben/tool-grounded-agent)**: a grounding harness for agentic drafting. Tool-ledger provenance plus a grounding backstop, with the system's own blind spots shipped as executable known-gap tests.
- **[grounded-rag](https://github.com/patrickiben/grounded-rag)**: retrieval with a grounding evaluator that flags unsupported claims and ungrounded numbers.
- **[calibrated-clinical-ml](https://github.com/patrickiben/calibrated-clinical-ml)**: from-scratch calibration and decision-curve evaluation, showing two predictors with identical AUC and very different calibration.
- **[guarded-llm-service](https://github.com/patrickiben/guarded-llm-service)**: the guardrail served over FastAPI with Docker, CI, and Prometheus-style metrics.

#### Decision-support

- **[public-data-consoles](https://github.com/patrickiben/public-data-consoles)**: 28 self-contained, browser-only dashboards on live public feeds (hazards and early warning, public health). Descriptive, not predictive.

<sub>Everything here uses public or synthetic data. Proofs of concept are labeled as such.</sub>
