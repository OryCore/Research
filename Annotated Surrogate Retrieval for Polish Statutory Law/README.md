# Annotated Surrogate Retrieval for Polish Statutory Law

Benchmark, per-question outputs and paired significance tests for the paper.

**Paper:** [arXiv:2608.30929](https://doi.org/10.48550/arXiv.2608.30929)

## Layout

```
├── test data/
│   ├── exam-adw-202X.json          # Parsed questions + answer keys
│   └── list/answers-20XX.pdf       # Official Ministry of Justice sources
│
├── data/
│   └── {2024, 2025}/               # Year-specific data
│       └── [method_name]/          # controls, dense, hybrid, lexical, or mine
│           ├── per_question.jsonl  # One row per question per configuration
│           ├── summary.json        # Aggregate metrics
│           ├── config.json         # Run parameters
│           ├── REPORT.md           # Rendered summary
│           └── tables/
│               ├── main.csv        # Core results
│               ├── all.csv
│               ├── cost.csv
│               └── retrieval.csv
│
├── mcnemar/
│   └── {2024, 2025}/               # Statistical significance tests by year
│       ├── mcnemar-*.csv           # Baseline full-hybrid (rank1, hit5, etc.)
│       └── mcnemar-*.json
│
└── results/
    └── {2024, 2025, Combined}/     # Final aggregated outputs
        ├── summary.json
        ├── REPORT.md
        └── tables/
```

## Benchmark at a glance

| Metric                          | Detail                                 |
| :------------------------------ | :------------------------------------- |
| **Questions**                   | 300 (150 per year, three options each) |
| **Reference citation resolved** | 291                                    |
| **Retrievable subset (`n*`)**   | 264 (133 in 2024, 131 in 2025)         |
| **Corpus**                      | 82,508 articles from 1,133 acts        |
| **Surrogate coverage**          | 22,241 articles (27.0%)                |
| **Configurations**              | 17 + 4 controls                        |

Six questions carry more than one reference article; `hit@k` credits any of them.

## Reading the numbers

- **`hit@k*`:** A reference article appears in the top _k_, calculated over the retrievable subset (`n*=264`).
- **`recall@k*`:** Fraction of reference articles retrieved. This differs from `hit@k*` only on the six multi-reference questions.
- **`citation_accuracy`:** The first cited article matches a reference (calculated over all 300 questions).
- **`accuracy`:** The correct option letter is chosen (calculated over all 300 questions).

## Notes

- 2023 examination PDFs are present but were not used in the paper.
- Models: `gemini-3.1-flash-lite` at temperature 0 for surrogate generation,
  query analysis, reranking and answer generation; `multilingual-e5-large` as
  the encoder.

## Licence

Code: [MIT](../Licenses/MIT).
Data and derived annotations: [CC BY 4.0](../Licenses/CC-BY-4.0).

Examination questions and answer keys are published by the Polish Ministry of
Justice; statutory texts are public.

## Citation

```bibtex
@misc{cengiz2026annotatedsurrogateretrievalpolish,
      title={Annotated Surrogate Retrieval for Polish Statutory Law},
      author={Orkun Yiğit Cengiz},
      year={2026},
      eprint={2608.30929},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2608.30929},
}
```
