# Bachelor Thesis — Vericult

LaTeX source for the bachelor thesis **Evidence-Grounded Verification of Cultural Appropriateness in Large Language Model Outputs**.

This repository is intentionally kept Overleaf-friendly: `main.tex` contains the complete current thesis source and `references.bib` contains the consolidated bibliography.

## Current freeze (pre-final experiments)

Completed and synchronized to the project state:
- Chapters 1–6: motivation, background, related work, D01–D10 framework, Vericult architecture, and final experimental methodology
- Chapter 9: threats to validity and limitations
- Appendices: rubric, semantic contracts, realized v1 human-annotation protocol, and reproducibility manifest
- Updated narrative: single-response verification is the primary use case; Best-of-4 is an evaluation mode
- Updated architecture: deterministic response spans and explicit contextual fallback when retrieval is insufficient
- Updated empirical plan: v1 development/stress set → backbone selection/freeze → realistic v2 → external validation

Intentionally left open until the frozen final experiments:
- Abstract
- Chapter 7 — Evaluation Results
- Chapter 8 — Error Analysis and Discussion
- Chapter 10 — Conclusion and Future Work

The current source compiles successfully with `pdflatex` + `biber` and produced a 72-page validation build on 2026-10-02.
