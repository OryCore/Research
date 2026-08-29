# Benchmark results
2026-08-23T19:45:48.334Z · 750 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `triad` | 150 | 133 | 96.7% | 78.2% | — | 80.3% | 0.6038 | 0.6448 | 71.3% | 0 |
| `rrf` | 150 | 133 | 96.0% | 72.9% | — | 78.5% | 0.6553 | 0.6793 | 69.3% | 0 |
| `dense-surro-rrf` | 150 | 133 | 96.7% | 71.4% | — | 75.1% | 0.6212 | 0.6453 | 67.3% | 0 |
| `dense-prf` | 150 | 133 | 93.3% | 70.7% | — | 73.9% | 0.5427 | 0.5843 | 64.0% | 0 |
| `dense-surro-rescore` | 150 | 133 | 88.0% | 64.7% | — | 66.0% | 0.4855 | 0.5192 | 58.7% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `triad` | 853 | 1090 | 102 | 1 | 4043 | 49 | $0.108 |
| `rrf` | 838 | 1256 | 90 | 1 | 4205 | 50 | $0.113 |
| `dense-surro-rrf` | 753 | 980 | 42 | 1 | 3918 | 50 | $0.105 |
| `dense-prf` | 750 | 949 | 56 | 1 | 3919 | 49 | $0.105 |
| `dense-surro-rescore` | 728 | 902 | 36 | 1 | 3925 | 48 | $0.105 |