<p align="center">
  <img src="https://raw.githubusercontent.com/Mochi-Sora/SoraAgent/main/assets/icon.png" alt="SoraAgent Benchmarks" width="96">
</p>

<h1 align="center">SoraAgent Benchmarks</h1>

<p align="center"><strong>Measured, not claimed.</strong></p>

<p align="center">
  <a href="https://github.com/Mochi-Sora/SoraAgent-Benchmarks/blob/main/SoraAgent-live-scoreboard.md"><img src="https://img.shields.io/badge/live%20score-86.3%2F100-6f42c1" alt="Live score 86.3/100"></a>
  <a href="https://github.com/Mochi-Sora/SoraAgent"><img src="https://img.shields.io/badge/SoraAgent-0.4.0-1f6feb" alt="SoraAgent 0.4.0"></a>
  <a href="https://github.com/Mochi-Sora/SoraAgent-Benchmarks/blob/main/SoraAgent-live-scoreboard.md"><img src="https://img.shields.io/badge/edge%20checks-54%2F54-2ea44f" alt="54 of 54 edge checks"></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-2ea44f" alt="MIT license"></a>
</p>

<p align="center">
  <a href="https://github.com/Mochi-Sora/SoraAgent">SoraAgent</a> ·
  <a href="https://mochi-sora.github.io/SoraOfficialWebsite/#benchmarks">Website</a> ·
  <a href="https://discord.gg/s8W6JfBSMH">Discord</a>
</p>

This repository publishes the public **SoraAgent live scoreboard**. The benchmark harness is maintained alongside the SoraAgent project; this repo is the stable, linkable record of each release's results.

SoraAgent Benchmarks is **not a leaderboard**. Every release is run through the same scenarios, and raw metrics matter more than the heuristic 0–100 scores. Weak suites stay visible.

## Latest result

| | |
| --- | --- |
| SoraAgent | **0.4.0** |
| Overall | **86.3 / 100 (B)** |
| Model | DeepSeek V4.1 Flash (`deepseek-flash`) |
| Mode | live, 78 model runs |
| Deterministic edge checks | **54 / 54** |
| Full report | [SoraAgent-live-scoreboard.md](SoraAgent-live-scoreboard.md) |

| Suite | Score |
| --- | ---: |
| Token usage | 67.9 |
| Tool-use accuracy | 89.4 |
| Memory retention | 95.1 |
| Dreaming mechanism | 100.0 |
| Response speed | 75.1 |
| Autonomous task completion | 65.0 |
| Prompt caching | 84.2 |
| Files, specialists, memory, graph & security | 100.0 |
| General instruction following | 100.0 |

## What is measured

- **Token usage** — prompt, completion, and effective tokens, including cache reuse.
- **Tool-use accuracy** — right tools, right arguments, right order, no unnecessary calls.
- **Memory retention** — retrieval hit rate, grounded answers, stale-fact handling, recall density.
- **Dreaming** — merge/conflict quality, inferred links, source retention, expiry, idempotence, cost.
- **Response speed** — end-to-end latency, provider/tool/framework time, tokens per second.
- **Autonomous task completion** — whether unrequested extra work is useful, neutral, or harmful.
- **Prompt caching** — reusable prefix size, stability, and what breaks the cache.
- **Files, specialists, memory, graph & security** — 54 deterministic edge checks covering documents, specialists, dream lifecycle, graph recall, state, provenance, channel auth, approvals, and output bounds.

## Reproduce it

The harness runs deterministic simulated scenarios and live-model scenarios from a checkout of the SoraAgent benchmark project. A run writes `report.json`, `summary.md`, `metrics.csv`, and `runs.jsonl` under `results/`.

```bash
# Deterministic, no API key
python3 run_benchmark.py

# Live model
export DEEPSEEK_API_KEY=...
python3 run_benchmark.py --mode live --provider deepseek \
  --model deepseek-flash --runs 2 --suites all
```

The published result above is the canonical source; raw metrics are in [SoraAgent-live-scoreboard.md](SoraAgent-live-scoreboard.md).

## Measurement quality

- Replicates are reported with Wilson confidence intervals for success rates and bootstrap intervals for continuous metrics.
- `--score-mode raw` suppresses the aggregate score while keeping every raw metric visible.
- Provider-reported token usage is preferred; `--tokenizer tiktoken` enables a model-specific counter when the optional package is installed.
- The **general** suite and `--adapter command` provide a portable surface for non-SoraAgent harnesses. SoraAgent-specific suites remain clearly labeled.

## License

The benchmark harness in this repository is **MIT-licensed**; see [`LICENSE`](LICENSE). SoraAgent itself is **AGPL-3.0-only**. © 2026 Tam Kuan Hou (譚君浩 / Marco Tam).
