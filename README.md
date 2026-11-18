<p align="center">
  <img src="https://raw.githubusercontent.com/Mochi-Sora/SoraAgent/main/assets/icon.png" alt="SoraAgent Benchmarks" width="96">
</p>

<h1 align="center">SoraAgent Benchmarks</h1>

<p align="center"><strong>Measured, not claimed.</strong></p>

<p align="center">
  <a href="https://github.com/Mochi-Sora/SoraAgent-Benchmarks/blob/main/SoraAgent-live-scoreboard.md"><img src="https://img.shields.io/badge/live%20score-84.4%2F100-6f42c1" alt="Live score 85.1/100"></a>
  <a href="https://github.com/Mochi-Sora/SoraAgent"><img src="https://img.shields.io/badge/SoraAgent-0.3.2-1f6feb" alt="SoraAgent 0.3.1"></a>
  <a href="https://github.com/Mochi-Sora/SoraAgent-Benchmarks/blob/main/SoraAgent-live-scoreboard.md"><img src="https://img.shields.io/badge/edge%20checks-54%2F54-2ea44f" alt="54 of 54 edge checks"></a>
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
| SoraAgent | **0.3.2** |
| Overall | **84.4 / 100 (B)** |
| Model | DeepSeek V4.1 Flash (`deepseek-flash`) |
| Mode | live, 62 model runs |
| Deterministic edge checks | **54 / 54** |
| Full report | [SoraAgent-live-scoreboard.md](SoraAgent-live-scoreboard.md) |

| Suite | Score |
| --- | ---: |
| Token usage | 67.0 |
| Tool-use accuracy | 92.0 |
| Memory retention | 95.1 |
| Dreaming mechanism | 100.0 |
| Response speed | 74.7 |
| Autonomous task completion | 62.9 |
| Prompt caching | 83.5 |
| Files, specialists, memory, graph & security | 100.0 |

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

## License

SoraAgent and this benchmark are **AGPL-3.0-only**. © 2026 Tam Kuan Hou (譚君浩 / Marco Tam).
