# Benchmark results
2026-08-23T20:15:14.809Z · 600 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `bm25-raw` | 150 | 131 | 96.7% | 74.0% | — | 79.0% | 0.6877 | 0.7083 | 68.0% | 0 |
| `bm25-lemma` | 150 | 131 | 97.3% | 73.3% | — | 78.2% | 0.6827 | 0.7031 | 68.0% | 0 |
| `bm25-surrogate` | 150 | 131 | 94.0% | 69.5% | — | 73.3% | 0.5845 | 0.6133 | 64.7% | 0 |
| `bm25-expanded` | 150 | 131 | 94.0% | 67.2% | — | 70.2% | 0.5922 | 0.6134 | 61.3% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `bm25-raw` | 709 | 983 | 24 | 1 | 4481 | 50 | $0.12 |
| `bm25-lemma` | 723 | 1037 | 42 | 1 | 4500 | 50 | $0.12 |
| `bm25-surrogate` | 671 | 980 | 10 | 1 | 3660 | 50 | $0.099 |
| `bm25-expanded` | 1817 | 2228 | 1129 | 2 | 4999 | 263 | $0.164 |