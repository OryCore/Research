# Benchmark results
2026-08-23T20:09:35.016Z · 600 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
Citation floor (closed-book) 52.7% · ceiling (oracle) 77.1%. `citation_gap_closed` is the fraction of that band a method recovers.
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `oracle` | 150 | 131 | 94.7% | 77.1% | 100.0% | 100.0% | 1 | 1 | 87.3% | 0 |
| `oracle-doc` | 150 | 131 | 80.7% | 42.0% | -43.8% | 11.5% | 0.0338 | 0.0445 | 9.3% | 0 |
| `closed-book` | 150 | 131 | 92.7% | 52.7% | 0.0% | 0.0% | 0 | 0 | 0.0% | 0 |
| `random` | 150 | 131 | 74.7% | 28.2% | -100.0% | 0.0% | 0 | 0 | 0.0% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `oracle` | 632 | 881 | 0 | 1 | 660 | 47 | $0.024 |
| `oracle-doc` | 665 | 819 | 3 | 1 | 3744 | 46 | $0.101 |
| `closed-book` | 657 | 870 | 0 | 1 | 292 | 45 | $0.014 |
| `random` | 670 | 966 | 0 | 1 | 4881 | 40 | $0.128 |