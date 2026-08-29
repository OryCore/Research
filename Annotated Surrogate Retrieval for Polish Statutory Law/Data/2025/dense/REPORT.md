# Benchmark results
2026-08-23T20:11:25.480Z · 300 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `dense-rephrased` | 150 | 131 | 94.7% | 72.5% | — | 74.1% | 0.596 | 0.6292 | 65.3% | 0 |
| `dense` | 150 | 131 | 94.0% | 67.9% | — | 71.4% | 0.6107 | 0.6337 | 62.7% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `dense-rephrased` | 1800 | 2173 | 1120 | 2 | 4672 | 263 | $0.156 |
| `dense` | 732 | 1101 | 44 | 1 | 3946 | 48 | $0.106 |