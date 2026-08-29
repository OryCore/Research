# Benchmark results
2026-08-23T19:30:01.720Z · 300 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `dense-rephrased` | 150 | 133 | 94.7% | 69.2% | — | 71.9% | 0.5653 | 0.5982 | 64.0% | 0 |
| `dense` | 150 | 133 | 90.7% | 66.9% | — | 70.5% | 0.5697 | 0.5986 | 62.7% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `dense-rephrased` | 1866 | 2216 | 1155 | 2 | 4656 | 260 | $0.155 |
| `dense` | 733 | 1064 | 48 | 1 | 4090 | 49 | $0.11 |