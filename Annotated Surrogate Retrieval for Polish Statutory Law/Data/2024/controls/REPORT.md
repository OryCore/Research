# Benchmark results
2026-08-23T19:28:28.131Z · 600 records · `gemini-3.1-flash-lite`
Metrics marked \* are over the **retrievable subset** (gold present in corpus).
Citation floor (closed-book) 52.6% · ceiling (oracle) 81.2%. `citation_gap_closed` is the fraction of that band a method recovers.
## Main
| Method | n | n\* | Acc | Citation | Gap closed | R@10\* | MRR\* | nDCG@10\* | Gold in ctx | Err |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `oracle` | 150 | 133 | 94.0% | 81.2% | 100.0% | 100.0% | 1 | 1 | 88.7% | 0 |
| `oracle-doc` | 150 | 133 | 76.0% | 43.6% | -31.6% | 4.0% | 0.0273 | 0.0206 | 3.3% | 0 |
| `closed-book` | 150 | 133 | 92.7% | 52.6% | 0.0% | 0.0% | 0 | 0 | 0.0% | 0 |
| `random` | 150 | 133 | 72.0% | 29.3% | -81.6% | 0.0% | 0.0001 | 0 | 0.0% | 0 |
## Cost & latency
| Method | p50 ms | p95 ms | retrieval p50 | LLM calls/q | tok in/q | tok out/q | USD/100q |
|---|---:|---:|---:|---:|---:|---:|---:|
| `oracle` | 636 | 864 | 0 | 1 | 660 | 47 | $0.024 |
| `oracle-doc` | 671 | 966 | 3 | 1 | 3749 | 46 | $0.101 |
| `closed-book` | 687 | 894 | 0 | 1 | 295 | 44 | $0.014 |
| `random` | 687 | 1065 | 0 | 1 | 4884 | 40 | $0.128 |