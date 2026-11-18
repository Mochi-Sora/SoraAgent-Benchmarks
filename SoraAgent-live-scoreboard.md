# SoraAgent — Live Benchmark Results

**Model:** DeepSeek V4.1 Flash (`deepseek-flash`)  
**Mode:** live OpenAI-compatible API  
**SoraAgent:** 0.3.2  
**Generated:** 2026-11-18T05:49:52+00:00  
**Duration:** 272.94 s  
**Scored agent runs:** 62  
**Deterministic edge checks:** 54/54 passed

## Overall

| Metric | Value |
| --- | ---: |
| Overall score | **84.4 / 100 (B)** |
| Total tokens per run | 9,213 tokens |
| Effective prompt cache hit rate | 80.4% |
| Scored edge checks | 54 / 54 |

## Suite scores

| Suite | Score | Scored runs |
| --- | ---: | ---: |
| Token usage | **67.0** | 8 |
| Tool-use accuracy | **92.0** | 20 |
| Memory retention | **95.1** | 14 |
| Dreaming mechanism | **100.0** | — |
| Response speed | **74.7** | 6 |
| Autonomous task completion | **62.9** | 12 |
| Prompt caching | **83.5** | 2 |
| Files, specialists, memory, graph & security | **100.0** | — |

## Headline metrics

| Metric | Value | Score |
| --- | ---: | ---: |
| Total tokens per run | 9,213 tokens | 59.7 / 100 |
| Successful tasks per 1k tokens | 0.11 tasks/1k | 43.4 / 100 |
| Tool selection F1 | 93.3% | 98.2 / 100 |
| Exact trajectory rate | 60.0% | 66.7 / 100 |
| Retrieval hit rate | 100.0% | 100.0 / 100 |
| End-to-end answer accuracy | 100.0% | 100.0 / 100 |
| Retained facts per 1k recall tokens | 27.18 facts/1k | 100.0 / 100 |
| Dream merge F1 | 100.0% | 100.0 / 100 |
| Dream conflict F1 | 100.0% | 100.0 / 100 |
| Duration per 100 memories | 0.32 | 100.0 / 100 |
| End-to-end latency (p95) | 6.86 s | 43.7 / 100 |
| Framework overhead (mean) | 19 ms | 100.0 / 100 |
| Net utility of extra actions | +0.00 utility/run | 50.0 / 100 |
| Harmful-extra execution rate | 0.0% | 100.0 / 100 |
| Effective prompt cache hit rate | 80.4% | 100.0 / 100 |
| Prompt cache stability | 25.3% | 25.3 / 100 |
| Message prefix stability | 92.8% | 100.0 / 100 |
| Stable prefix tokens | 1,235 tokens | 100.0 / 100 |
| Edge-case checks passed | 100.0 | 100.0 / 100 |

## Token usage

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Prompt tokens per run | 8,814 tokens | 56.7 / 100 | lower is better |
| Completion tokens per run | 398 tokens | 100.0 / 100 | lower is better |
| Total tokens per run | 9,213 tokens | 59.7 / 100 | lower is better |
| Effective tokens per run (after prefix reuse) | 2,013 tokens | 100.0 / 100 | lower is better |
| Tokens per successful task | 9,213 tokens | 54.3 / 100 | lower is better |
| Successful tasks per 1k tokens | 0.11 tasks/1k | 43.4 / 100 | higher is better |
| Static prompt overhead share | 60.5% | 91.0 / 100 | lower is better |
| Tool-schema token share | 30.9% | 100.0 / 100 | lower is better |
| Prompt tokens reused by prefix cache | 81.7% | 100.0 / 100 | higher is better |
| Provider-reported usage available | yes | — | higher is better |

## Tool-use accuracy

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Tool selection F1 | 93.3% | 98.2 / 100 | higher is better |
| Tool selection precision | 95.0% | 100.0 / 100 | higher is better |
| Tool selection recall | 95.0% | 100.0 / 100 | higher is better |
| Exact trajectory rate | 60.0% | 66.7 / 100 | higher is better |
| Argument accuracy | 81.7% | 86.0 / 100 | higher is better |
| Forbidden tool rate | 0.0% | 100.0 / 100 | lower is better |
| Unnecessary call rate | 5.0% | 100.0 / 100 | lower is better |
| Task success rate | 95.0% | 100.0 / 100 | higher is better |
| Tool error rate | 0.0% | 100.0 / 100 | lower is better |
| Approval compliance | 100.0% | 100.0 / 100 | higher is better |
| Discovery calls per run | 1.05 calls | 100.0 / 100 | lower is better |
| Business calls per run | 1.50 calls | — | higher is better |
| First business call correct | 90.0% | 90.0 / 100 | higher is better |

## Memory retention

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Retrieval hit rate | 100.0% | 100.0 / 100 | higher is better |
| Retrieval precision | 83.3% | 100.0 / 100 | higher is better |
| Mean reciprocal rank | 94.4% | 100.0 / 100 | higher is better |
| Contradicting/forbidden fact rate | 16.7% | 30.0 / 100 | lower is better |
| No-answer false-positive rate | 0.0% | 100.0 / 100 | lower is better |
| End-to-end answer accuracy | 100.0% | 100.0 / 100 | higher is better |
| Recall-first compliance | 100.0% | 100.0 / 100 | higher is better |
| Answer grounded in recall | 100.0% | 100.0 / 100 | higher is better |
| Memory write-through rate | 100.0% | 100.0 / 100 | higher is better |
| Retained facts per 1k recall tokens | 27.18 facts/1k | 100.0 / 100 | higher is better |
| Recall payload tokens per query | 48 tokens | 100.0 / 100 | lower is better |
| Relevant-character density | 34.5% | 62.8 / 100 | higher is better |
| Corpus-to-recall compression | 6.51 x | — | higher is better; Corpus-size dependent; informational in this fixture. |
| Recall latency | 3.2 ms | 100.0 / 100 | lower is better |
| Memory efficiency sub-score | 90.7 | — | higher is better |

### Memory queries

| Query | Hit | Precision | Tokens | MRR |
| --- | --- | ---: | ---: | ---: |
| codename | yes | 25.0% | 131 | 1.00 |
| seat | yes | 50.0% | 62 | 1.00 |
| badge | yes | 100.0% | 27 | 1.00 |
| deploy | yes | 25.0% | 131 | 0.33 |
| owner | yes | 100.0% | 32 | 1.00 |
| budget | yes | 100.0% | 36 | 1.00 |
| sla | yes | 100.0% | 32 | 1.00 |
| acme | yes | 100.0% | 30 | 1.00 |
| retention | yes | 100.0% | 26 | 1.00 |
| datacenter | yes | 100.0% | 26 | 1.00 |
| portal | yes | 100.0% | 25 | 1.00 |
| cjk | yes | 100.0% | 58 | 1.00 |
| none | yes | 100.0% | 8 | 1.00 |


## Dreaming mechanism

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Dream merge F1 | 100.0% | 100.0 / 100 | higher is better |
| Dream merge precision | 100.0% | 100.0 / 100 | higher is better |
| Dream merge recall | 100.0% | 100.0 / 100 | higher is better |
| Dream conflict F1 | 100.0% | 100.0 / 100 | higher is better |
| Dream inference F1 | 100.0% | 100.0 / 100 | higher is better |
| Source-memory retention | 100.0% | 100.0 / 100 | higher is better |
| Expiry accuracy | 100.0% | 100.0 / 100 | higher is better |
| Artifact cleanup rate | 100.0% | 100.0 / 100 | higher is better |
| Idempotent on rerun | yes | 100.0 / 100 | higher is better |
| Dream error rate | 0.0% | 100.0 / 100 | lower is better |
| Duration per 100 memories | 0.319 s | 100.0 / 100 | lower is better |
| Backend calls per memory | 5.92 calls | 100.0 / 100 | lower is better |
| Memories consolidated per second | 313.73 mem/s | 100.0 / 100 | higher is better |
| Actions per memory | 4.31 actions | 100.0 / 100 | lower is better |
| Wake-model tokens per call | 10 tokens | 100.0 / 100 | lower is better |
| Wake-model calls | 1.00 calls | — | lower is better |
| Wake-model tokens (total) | 10 tokens | — | lower is better |
| Dream report size | 11,299 bytes | — | lower is better |
| Merge yield vs expected | 100.0% | 100.0 / 100 | higher is better |
| Daily messages consolidated | 3 messages | — | higher is better |

### Dream expectations vs. observed

- Merge groups: observed 2 / expected 2
- Conflict pairs: observed 1 / expected 1
- Inferred pairs: observed 1 / expected 1
- Source retention: 12 / 12


## Response speed

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| End-to-end latency (mean) | 4.74 s | 31.6 / 100 | lower is better |
| End-to-end latency (p95) | 6.86 s | 43.7 / 100 | lower is better |
| Provider time (mean) | 4.72 s | 31.8 / 100 | lower is better |
| Tool time (mean) | 1.9 ms | 100.0 / 100 | lower is better |
| Framework overhead (mean) | 19.4 ms | 100.0 / 100 | lower is better |
| Framework overhead (p95) | 28.7 ms | 100.0 / 100 | lower is better |
| Framework overhead share | 0.4% | 100.0 / 100 | lower is better |
| Latency per step | 1173.9 ms/step | 68.1 / 100 | lower is better |
| Latency per provider call | 1168.6 ms/call | 64.2 / 100 | lower is better |
| Completion tokens per second | 69.74 tok/s | 100.0 / 100 | higher is better |
| Tasks per second | 0.23 tasks/s | 11.3 / 100 | higher is better |

## Autonomous task completion

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Net utility of extra actions | +0.00 utility/run | 50.0 / 100 | higher is better; Labeled weights: helpful actions are positive, harmful actions are negative; only executed extras count. |
| Useful-extra precision | 0.0% | 0.0 / 100 | higher is better |
| Useful opportunity recall | 0.0% | 0.0 / 100 | higher is better |
| Extra actions judged useful | 0.0% | 0.0 / 100 | higher is better |
| Harmful-extra execution rate | 0.0% | 100.0 / 100 | lower is better |
| Harmful-extra attempt rate | 0.0% | 100.0 / 100 | lower is better |
| Runs with negative impact | 0.0% | 100.0 / 100 | lower is better |
| Duplicate/extraneous action rate | 0.0% | 100.0 / 100 | lower is better; Extras that repeat a requested action or an earlier extra exactly. |
| Runs with extra actions | 0.0% | — | higher is better |
| Extra actions per run | 0.00 actions | — | higher is better |
| Requested task success | 91.7% | 91.7 / 100 | higher is better |
| Extra consequential actions gated | 100.0% | 100.0 / 100 | higher is better |

## Prompt caching

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Prompt prefix cache hit rate | 51.8% | 86.3 / 100 | higher is better; Predicted share of prompt tokens reusable as a byte-for-byte prefix; this is conservative when tools precede messages. |
| Effective prompt cache hit rate | 80.4% | 100.0 / 100 | higher is better; Provider-reported cache hit rate when available, otherwise the predicted prefix hit rate. |
| Message prefix cache hit rate | 69.1% | 98.7 / 100 | higher is better; Prompt-cache reuse after excluding tool schemas; isolates system-prompt/conversation ordering from tool-catalog churn. |
| Message prefix stability | 92.8% | 100.0 / 100 | higher is better; Prefix retention for system prompt and conversation only, excluding tool schemas. |
| Prompt cache stability | 25.3% | 25.3 / 100 | higher is better; Mean prefix retention penalized by its variation across turns. |
| Stable prefix tokens | 1,235 tokens | 100.0 / 100 | higher is better |
| Cacheable request rate | 75.0% | 100.0 / 100 | higher is better |
| Mean prefix retention | 66.2% | 100.0 / 100 | higher is better |
| Worst prefix retention | 0.4% | 1.5 / 100 | higher is better |
| Tool-schema churn per transition | 37.5% | 62.5 / 100 | lower is better |
| Clock churn per transition | 100.0% | — | lower is better; Clock content changes are expected; what matters is whether the clock is trailing. See trailing rate. |
| Clock in trailing position | 100.0% | 100.0 / 100 | higher is better; Fraction of clock-bearing requests where ## CURRENT TIME is the final message, after the conversation. |
| Identity churn per transition | 0.0% | 100.0 / 100 | lower is better |
| Prefix breaks per run | 1.50 breaks | 70.0 / 100 | lower is better |
| First prompt identical across runs | yes | 100.0 / 100 | higher is better |
| Cache hit-rate variation across runs | 5.3% | 94.7 / 100 | lower is better |
| Reused prompt tokens | 8,580 tokens | — | higher is better |
| Total prompt tokens | 16,578 tokens | — | lower is better |
| Provider-reported cache hit rate | 80.4% | 100.0 / 100 | higher is better |
| Provider-reported cache counters available | yes | — | higher is better |
| Predicted vs reported cache-rate error | 28.6% | 71.4 / 100 | lower is better |

### Cache ablation

| Variant | Hit rate | Stability | Cached tokens | Prompt tokens |
| --- | ---: | ---: | ---: | ---: |
| full | 51.8% | 25.3% | 8580 | 16578 |

**Cache diagnosis:** the clock changes every turn but is trailing, so it no longer invalidates the cached prefix


## Files, specialists, memory, graph & security

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Files edge checks | 100.0 | 100.0 / 100 | higher is better; 12/12 checks passed |
| Specialists edge checks | 100.0 | 100.0 / 100 | higher is better; 14/14 checks passed |
| Memory Modes edge checks | 100.0 | 100.0 / 100 | higher is better; 8/8 checks passed |
| Graph Memory edge checks | 100.0 | 100.0 / 100 | higher is better; 5/5 checks passed |
| Security edge checks | 100.0 | 100.0 / 100 | higher is better; 15/15 checks passed |
| Edge-case checks passed | 100.0 | 100.0 / 100 | higher is better; 54/54 checks passed |

---

Scores are heuristic normalizations against explicit targets; inspect the raw metrics and diagnostics before drawing conclusions.  Simulated mode is a deterministic reference policy, not a model ranking.

## Edge-case coverage

The deterministic **Files, specialists, memory, graph & security** suite ran alongside the live suites:

- **Files (12/12):** DOCX, ODF, EPUB, RTF, EML, nested ZIP/TAR, HTML script stripping, HTML tables, empty files, malformed DOCX, archive total-byte caps, wide-CSV fallback.
- **Specialists (14/14):** manifest round-trip, lexical routing, forbidden delegation-control tools, scoped registry, worker spawning, workspace escape rejection, SQLite daily stores, daily recall, provisional creation, unsafe-tool stripping, quotas.
- **Memory modes (8/8):** specialist daily transfer provenance, daily clearing, half-done round, second-round completion, failed-transfer queue, final forget, daily-only dedupe, lossless archive.
- **Graph/memory (5/5):** graph extraction, graph-aware recall facts, native graph projection, transient inferred-link cleanup, missing-memory HTTP 404.
- **Security/state (15/15):** session-state ids, leading system prompt, identity/state provenance, daily session scope, durable merge, decay progress, tool-output framing, redirect/peer guards, calendar approvals, exact approval words, iMessage secret requirement, attachment caps, execute-code bounds.

No suite errors. The two warnings in the log are expected security checks proving that identity/state edits from tool-output turns are ignored.
