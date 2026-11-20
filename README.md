# PDF Prompt Injection in Legal AI

**Experimental artifacts and reproducibility materials for:**

*Prompt Injection in PDF Documents: Risks to LLM-Assisted Procedural Analysis and Legal Draft Generation*

**Conference:** ICAART 2027 (Short Paper)

## Overview

This repository supports research on document-borne prompt injection in AI-assisted procedural analysis and legal draft generation. The study evaluates whether adversarial instructions incorporated into PDF documents are associated with deviations from legitimate tasks and changes in the substantive orientation of generated legal drafts.

The evaluation was conducted through publicly accessible, provider-operated web interfaces. Consequently, findings concern deployed end-to-end systems, including document ingestion and preprocessing, rather than isolated language models.

## Study design

The methodology comprises two phases:

- **Phase I — Controlled screening:** 27 PDF-borne injection techniques evaluated on four LLM-based systems, with three separate conversational executions per system–technique condition (324 executions). A technique advanced to Phase II if at least one injection-consistent response was observed in at least two distinct systems.
- **Phase II — Contextualized legal drafting:** 16 selected techniques evaluated using one anonymized real judicial petition. Each system's baseline orientation was established from three executions of the unmodified petition. Adversarial conditions targeted the opposite substantive orientation, with three repetitions per condition.

The study reports Attack Success Rate (ASR), Contextual Attack Success Rate (CASR), and Contextual Susceptibility Score (CS). Results are descriptive and should not be interpreted as generalizable attack success probabilities.

## Repository status

**Status: Repository initialized; experimental artifacts pending release.**

The repository is being prepared to host study materials. Not all materials described below are available yet. Availability and completeness will be updated here as files are released. Do not interpret this initial README as a claim that the experimental dataset has already been published.

## Planned structure

```text
.
├── README.md
├── LICENSE                       # To be selected
├── docs/
│   ├── experimental-protocol.md
│   └── technique-catalog.md
├── phase1/
│   ├── pdfs/                     # PDF examples, organized by technique ID
│   ├── prompts/
│   └── results/
├── phase2/
│   ├── pdfs/                     # Privacy-reviewed/anonymized materials only
│   ├── prompts/
│   └── results/
├── metadata/
│   ├── systems-and-periods.csv
│   └── execution-log-schema.csv
└── scripts/                       # Shareable document-generation/analysis scripts
```

Directories and files will be added progressively. This tree describes the *planned* organization, not files currently present.

## Technique identifiers

The study uses stable IDs **1–27** for the Phase I PDF-borne techniques. The 16 techniques retained for Phase II were:

`1, 2, 3, 5, 6, 8, 9, 10, 11, 15, 16, 17, 24, 25, 26, 27`

When released, the technique catalog will map each ID to its operational definition and corresponding example materials.

## Privacy, legal, and security considerations

The Phase II case derives from a judicial proceeding. Only materials that have been reviewed for personal information, confidentiality, and applicable disclosure obligations will be published. Some original files, prompts, or execution logs may require redaction, substitution, or exclusion.

The PDF examples contain adversarial instructions intended for controlled security research. Treat all repository PDFs as **untrusted input**. Do not upload them to live case-management systems or use them in production legal workflows. Conduct reproduction only in authorized test environments.

## Limitations

- Phase II involves **one judicial petition** and **three repetitions per experimental condition**.
- The systems were accessed through provider web interfaces; internal preprocessing and model configurations could not be isolated.
- Transformation-only benign controls were not included, so instruction effects cannot be separated causally from PDF-transformation effects.
- Draft classifications were reviewed within the research team; no independent blinded assessment or inter-rater agreement measurement was conducted.

## Citation

If referring to the research results, cite the corresponding ICAART 2027 paper. Once this repository is publicly available, it may be cited as a supplementary research resource:

```bibtex
@misc{ramos2026pdfdataset,
  author = {Ramos, Rafael Marconi and Pacheco, {\'E}zio Paes and
            Omati, Jo{\~a}o Victor Rodrigues Viana and
            Jesus, Oliver Henrique Ferreira de and
            Brom, Pedro Carvalho and Weigang, Li},
  title = {PDF Prompt Injection in Legal AI: Experimental Artifacts and Reproducibility},
  year = {2026},
  howpublished = {GitHub repository},
  url = {https://github.com/SEU-USUARIO/pdf-prompt-injection-legal-ai},
  note = {Experimental artifacts pending release}
}
```

Replace `SEU-USUARIO` with the GitHub owner before publishing or citing the repository. Update the citation and release status as artifacts become available.

## Contact and updates

For research-related questions, use the repository's **Issues** section after it is enabled. Updates to the release status and material inventory will be documented in this README.
