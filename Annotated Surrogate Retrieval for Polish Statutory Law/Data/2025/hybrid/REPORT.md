# Benchmark results
2026-08-23T20:19:06.290Z · 750 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `dense-surro-rrf` | 150 | 131 | 98.7% | 75.6% | — | 82.4% | 0.6651 | 0.7006 | 72.7% | 0 |
| `triad` | 150 | 131 | 96.7% | 76.3% | — | 82.4% | 0.6327 | 0.6732 | 72.0% | 0 |
| `rrf` | 150 | 131 | 97.3% | 75.6% | — | 81.3% | 0.7176 | 0.738 | 71.3% | 0 |
| `dense-prf` | 150 | 131 | 96.0% | 70.2% | — | 74.4% | 0.5717 | 0.6085 | 65.3% | 0 |
| `dense-surro-rescore` | 150 | 131 | 92.0% | 64.9% | — | 66.8% | 0.4947 | 0.5328 | 58.0% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `dense-surro-rrf` | 731 | 1129 | 42 | 1 | 3955 | 50 | $0.106 |
| `triad` | 795 | 1085 | 109 | 1 | 4030 | 49 | $0.108 |
| `rrf` | 809 | 1183 | 107 | 1 | 4283 | 49 | $0.114 |
| `dense-prf` | 714 | 961 | 51 | 1 | 3877 | 49 | $0.104 |
| `dense-surro-rescore` | 701 | 1089 | 37 | 1 | 3995 | 49 | $0.107 |