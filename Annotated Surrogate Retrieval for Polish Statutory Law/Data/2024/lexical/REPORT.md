# Benchmark results
2026-08-23T19:38:16.577Z · 600 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `bm25-lemma` | 150 | 133 | 97.3% | 75.2% | — | 73.9% | 0.65 | 0.6646 | 66.0% | 0 |
| `bm25-raw` | 150 | 133 | 95.3% | 70.7% | — | 72.1% | 0.6673 | 0.672 | 64.0% | 0 |
| `bm25-expanded` | 150 | 133 | 96.7% | 69.9% | — | 69.8% | 0.5681 | 0.5909 | 61.3% | 0 |
| `bm25-surrogate` | 150 | 133 | 92.7% | 66.9% | — | 67.9% | 0.5227 | 0.5549 | 61.3% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `bm25-lemma` | 752 | 986 | 41 | 1 | 4389 | 49 | $0.117 |
| `bm25-raw` | 747 | 1056 | 26 | 1 | 4332 | 49 | $0.116 |
| `bm25-expanded` | 1888 | 2234 | 1178 | 2 | 5074 | 261 | $0.166 |
| `bm25-surrogate` | 680 | 941 | 10 | 1 | 3560 | 50 | $0.097 |