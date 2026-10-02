# Bachelor Thesis — Vericult

LaTeX source for the bachelor thesis **“Vericult: Evidence-Grounded Verification of Cultural Appropriateness in Large Language Model Outputs.”**

## Current pre-final-experiment freeze

Completed and synchronized to the current project state:

- Chapters 1–6: motivation, background, related work, D01–D10 framework, Vericult architecture, and experimental methodology.
- Chapter 9: threats to validity and limitations.
- Appendices: runtime rubric, semantic prompt contracts, realized v1 human-annotation protocol, and reproducibility manifest.
- Single-response verification is the primary intended use case; Best-of-4 is retained as a comparative evaluation protocol.
- The architecture reflects deterministic response-span grounding and the explicit contextual fallback for evidence-unresolved dimensions.
- v1 is treated as development/stress material; v2 is the realistic confirmatory regime.
- Backbone selection occurs before the final semantic freeze.
- CARB and complementary published cultural benchmarks are used only after freeze for external validation.

Intentionally left as TODO until the final experiments:

- Abstract
- Chapter 7 — Evaluation Results
- Chapter 8 — Error Analysis and Discussion
- Chapter 10 — Conclusion and Future Work

The bibliography is consolidated in `references.bib`. The final empirical manifest will replace the remaining explicitly marked “to be frozen / to be recorded” fields once the backbone, v2 dataset, v2 human reference, external sample, and analysis seeds are fixed.

Compile with an Overleaf/Biber-capable LaTeX environment using `main.tex`.
