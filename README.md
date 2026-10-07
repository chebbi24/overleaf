# Bachelor Thesis — Vericult

LaTeX source for the bachelor thesis **“Vericult: Evidence-Grounded Verification of Cultural Appropriateness in Large Language Model Outputs.”**

## Definitive pre-results manuscript freeze

The report is synchronized to the restored and revalidated Vericult 1.1 repository:

- semantic/code freeze: `286598d5eb642c3d632e7b756ccf1954fb922a13`;
- final repository snapshot: `cc2de515cc481a6ec82c8c3edd5611209b84e97b`;
- stable refs `main`, `agent/final-experiment-ready`, and `freeze/vericult-v1.1-thesis` point to that final snapshot;
- verifier backbone: local Ollama `qwen3:4b`, temperature 0;
- prompt-level cultural-applicability gate → `not_culturally_applicable`;
- per-response assessability gate → `not_assessable` for pure refusals/non-answers;
- deterministic response-span grounding with normalized equivalent span IDs and Python-derived retrieval routing;
- candidate-blind evidence acquisition with LIVE → audited freeze → primary REPLAY;
- dimension scores `0/1/2/abstain`;
- selective recommendation fallback only for evidence-unresolved context-dependent recommendations;
- substantive labels `culturally_appropriate`, `partially_culturally_appropriate`, `culturally_inappropriate`;
- additional selective outcome `insufficient_evidence` for applicable/assessable cases with no defensible scored basis;
- Best-of-4 outcomes include candidate winner, `no_clear_winner`, `no_acceptable_candidate`, `insufficient_evidence`, `not_culturally_applicable`, and `not_assessable`;
- frozen controlled benchmark: PLT001–PLT030, 120 candidates, Human Gold v1;
- independent baselines: Skywork Reward V2 and a direct no-retrieval `qwen3:4b` judge;
- preregistered post-freeze external protocol: SafeWorld, CultureLLM/WVS, ScopeBench, and conditional CARB.

The definitive freeze restores the validated October 5 `fix/cultural120-result-semantics` repair (`c1944bb1df47a8668689c316e62563bdc700fbf3`) that had been used for the final failed-item rerun of the 120-case cross-dataset experiment but was accidentally left unmerged when the earlier freeze was assembled. The restoration was selectively applied to the cleaned code tree and revalidated by GitHub Actions run `37608473802`.

Chapters 1–6 and 9 plus the appendices are intended to be final before the remaining frozen experiments. Chapters 7, 8 and 10 contain structured result/discussion/conclusion placeholders. The abstract is complete except for the final quantitative sentence for the frozen PLT/baseline/post-freeze external runs.

## Empirical cross-dataset validation

The thesis also reports the completed pre-freeze 120-item positive-control validation: 20 each from CARE, Community Alignment, PLURAL, PACT, ThaiCLI and PRISM. After reruns, 116/120 completed. The four unresolved records are 028, 034 and 084 (transport `ReadTimeout`) and 076 (target-extraction structural failure).

The exact corpus and final post-rerun result export are preserved on `chebbi24/cultural-verification-thesis` branch `archive/external-120-pre-freeze`, commit `3a7bd8088ca1f9cabc8b7945792430cc501c160d`. The run is treated as positive-control/robustness evidence rather than a balanced accuracy benchmark. Its applicability/non-applicability semantics match the restored final verifier, but the compact result export does not embed an exact runtime Git SHA, so it remains reported separately from the definitive frozen experiment.

The bibliography is consolidated in `references.bib`. Runtime-only information such as the exact local Ollama digest and execution dates is captured by the frozen preflight/results manifests and inserted after execution; it does not reopen the semantic methodology.

Compile with an Overleaf/Biber-capable LaTeX environment using `main.tex`.
