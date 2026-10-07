# Bachelor Thesis — Vericult

LaTeX source for the bachelor thesis **“Vericult: Evidence-Grounded Verification of Cultural Appropriateness in Large Language Model Outputs.”**

## Pre-results manuscript freeze

The report is synchronized to the frozen Vericult 1.1 repository:

- semantic/code freeze: `200bca4575304795f491e76308d9be327ca269da`;
- final repository snapshot: `09257316c52f6c82eab405dbf2f8e2aff37f9b97`;
- verifier backbone: local Ollama `qwen3:4b`, temperature 0;
- deterministic response-span grounding;
- candidate-blind evidence acquisition with LIVE → audited freeze → primary REPLAY;
- dimension scores `0/1/2/abstain`;
- candidate labels `culturally_appropriate`, `partially_culturally_appropriate`, `culturally_inappropriate`, and selective `insufficient_evidence`;
- Best-of-4 outcomes include candidate winner, `no_clear_winner`, `no_acceptable_candidate`, and `insufficient_evidence`;
- frozen controlled benchmark: PLT001–PLT030, 120 candidates, Human Gold v1;
- independent baselines: Skywork Reward V2 and a direct no-retrieval `qwen3:4b` judge;
- preregistered post-freeze external protocol: SafeWorld, CultureLLM/WVS, ScopeBench, and conditional CARB.

Chapters 1–6 and 9 plus the four appendices are intended to be final before results. Chapters 7, 8 and 10 contain structured placeholders that are populated only after the frozen empirical runs. The abstract is complete except for its final quantitative result sentence.

The bibliography is consolidated in `references.bib`. Runtime-only information such as the exact local Ollama digest and execution dates is captured by the frozen preflight/results manifests and inserted after execution; it does not reopen the semantic methodology.

Compile with an Overleaf/Biber-capable LaTeX environment using `main.tex`.
