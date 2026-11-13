# SoraAgent — Live Benchmark Results

**Model:** DeepSeek V4.1 Flash (`deepseek-flash`)  
**Mode:** live OpenAI-compatible API  
**Generated:** 2026-11-12T12:27:38Z  
**Duration:** 290.92 s  
**Scored agent runs:** 62 across all seven suites  

## Overall

| Metric | Value |
| --- | ---: |
| Overall score | **82.4 / 100 (B)** |
| Total tokens | 356,763 |
| Prompt tokens | 333,456 |
| Completion tokens | 23,307 |
| Cached prompt tokens | 278,772 |
| Provider cache hit rate | 83.6% |

## Suite scores

| Suite | Score | Scored runs |
| --- | ---: | ---: |
| Token usage | **69.7** | 8 |
| Tool-use accuracy | **91.1** | 20 |
| Memory retention | **94.8** | 14 |
| Dreaming mechanism | **100.0** | — |
| Response speed | **74.0** | 6 |
| Autonomous task completion | **62.9** | 12 |
| Prompt caching | **84.3** | 2 |

## Headline metrics

| Metric | Value | Score |
| --- | ---: | ---: |
| Total tokens per run | 8,194 tokens | 67.1 / 100 |
| Successful tasks per 1k tokens | 0.12 tasks/1k | 48.8 / 100 |
| Tool selection F1 | 93.3% | 98.2 / 100 |
| Exact trajectory rate | 60.0% | 66.7 / 100 |
| Retrieval hit rate | 100.0% | 100.0 / 100 |
| End-to-end answer accuracy | 100.0% | 100.0 / 100 |
| Retained facts per 1k recall tokens | 25.84 facts/1k | 100.0 / 100 |
| Dream merge F1 | 100.0% | 100.0 / 100 |
| Dream conflict F1 | 100.0% | 100.0 / 100 |
| Duration per 100 memories | 0.325 s | 100.0 / 100 |
| End-to-end latency (p95) | 7.09 s | 42.3 / 100 |
| Framework overhead (mean) | 13.5 ms | 100.0 / 100 |
| Net utility of extra actions | +0.00 utility/run | 50.0 / 100 |
| Harmful-extra execution rate | 0.0% | 100.0 / 100 |
| Effective prompt cache hit rate | 83.7% | 100.0 / 100 |
| Prompt cache stability | 28.9% | 28.9 / 100 |
| Message prefix stability | 92.6% | 100.0 / 100 |
| Stable prefix tokens | 1,230 tokens | 100.0 / 100 |

## Token usage

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Prompt tokens per run | 7,835 tokens | 63.8 / 100 | lower is better |
| Completion tokens per run | 359 tokens | 100.0 / 100 | lower is better |
| Total tokens per run | 8,194 tokens | 67.1 / 100 | lower is better |
| Effective tokens per run (after prefix reuse) | 1,746 tokens | 100.0 / 100 | lower is better |
| Tokens per successful task | 8,194 tokens | 61.0 / 100 | lower is better |
| Successful tasks per 1k tokens | 0.12 tasks/1k | 48.8 / 100 | higher is better |
| Static prompt overhead share | 63.3% | 86.9 / 100 | lower is better |
| Tool-schema token share | 32.9% | 100.0 / 100 | lower is better |
| Prompt tokens reused by prefix cache | 82.3% | 100.0 / 100 | higher is better |
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
| Task success rate | 90.0% | 94.7 / 100 | higher is better |
| Tool error rate | 0.0% | 100.0 / 100 | lower is better |
| Approval compliance | 100.0% | 100.0 / 100 | higher is better |
| Discovery calls per run | 1.30 calls | 100.0 / 100 | lower is better |
| Business calls per run | 1.50 calls | — | higher is better |
| First business call correct | 90.0% | 90.0 / 100 | higher is better |

## Memory retention

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| Retrieval hit rate | 100.0% | 100.0 / 100 | higher is better |
| Retrieval precision | 83.3% | 100.0 / 100 | higher is better |
| Mean reciprocal rank | 100.0% | 100.0 / 100 | higher is better |
| Contradicting/forbidden fact rate | 16.7% | 30.0 / 100 | lower is better |
| No-answer false-positive rate | 0.0% | 100.0 / 100 | lower is better |
| End-to-end answer accuracy | 100.0% | 100.0 / 100 | higher is better |
| Recall-first compliance | 100.0% | 100.0 / 100 | higher is better |
| Answer grounded in recall | 85.7% | 85.7 / 100 | higher is better |
| Memory write-through rate | 100.0% | 100.0 / 100 | higher is better |
| Retained facts per 1k recall tokens | 25.84 facts/1k | 100.0 / 100 | higher is better |
| Recall payload tokens per query | 48 tokens | 100.0 / 100 | lower is better |
| Relevant-character density | 32.2% | 58.5 / 100 | higher is better |
| Corpus-to-recall compression | 6.14 x | — | higher is better; Corpus-size dependent; informational in this fixture. |
| Recall latency | 3.1 ms | 100.0 / 100 | lower is better |
| Memory efficiency sub-score | 89.6 | — | higher is better |

### Memory queries

| Query | Hit | Precision | Tokens | MRR |
| --- | --- | ---: | ---: | ---: |
| codename | yes | 25.0% | 126 | 1.00 |
| seat | yes | 50.0% | 62 | 1.00 |
| badge | yes | 100.0% | 29 | 1.00 |
| deploy | yes | 25.0% | 126 | 1.00 |
| owner | yes | 100.0% | 33 | 1.00 |
| budget | yes | 100.0% | 38 | 1.00 |
| sla | yes | 100.0% | 33 | 1.00 |
| acme | yes | 100.0% | 32 | 1.00 |
| retention | yes | 100.0% | 28 | 1.00 |
| datacenter | yes | 100.0% | 28 | 1.00 |
| portal | yes | 100.0% | 27 | 1.00 |
| cjk | yes | 100.0% | 59 | 1.00 |
| none | yes | 100.0% | 8 | 1.00 |


## Dreaming mechanism

| Metric                           |        Value | Target/Score | Interpretation   |
| -------------------------------- | -----------: | -----------: | ---------------- |
| Dream merge F1                   |       100.0% |  100.0 / 100 | higher is better |
| Dream merge precision            |       100.0% |  100.0 / 100 | higher is better |
| Dream merge recall               |       100.0% |  100.0 / 100 | higher is better |
| Dream conflict F1                |       100.0% |  100.0 / 100 | higher is better |
| Dream inference F1               |       100.0% |  100.0 / 100 | higher is better |
| Source-memory retention          |       100.0% |  100.0 / 100 | higher is better |
| Expiry accuracy                  |       100.0% |  100.0 / 100 | higher is better |
| Artifact cleanup rate            |       100.0% |  100.0 / 100 | higher is better |
| Idempotent on rerun              |          yes |  100.0 / 100 | higher is better |
| Dream error rate                 |         0.0% |  100.0 / 100 | lower is better  |
| Duration per 100 memories        |      0.325 s |  100.0 / 100 | lower is better  |
| Backend calls per memory         |   5.85 calls |  100.0 / 100 | lower is better  |
| Memories consolidated per second | 307.69 mem/s |  100.0 / 100 | higher is better |
| Actions per memory               | 4.23 actions |  100.0 / 100 | lower is better  |
| Wake-model tokens per call       |    10 tokens |  100.0 / 100 | lower is better  |
| Wake-model calls                 |   1.00 calls |            — | lower is better  |
| Wake-model tokens (total)        |    10 tokens |            — | lower is better  |
| Dream report size                | 11,157 bytes |            — | lower is better  |
| Merge yield vs expected          |       100.0% |  100.0 / 100 | higher is better |
| Daily messages consolidated      |   3 messages |            — | higher is better |

### Dream expectations vs. observed

- Merge groups: observed 2 / expected 2
- Conflict pairs: observed 1 / expected 1
- Inferred pairs: observed 1 / expected 1
- Source retention: 12 / 12


## Response speed

| Metric | Value | Target/Score | Interpretation |
| --- | ---: | ---: | --- |
| End-to-end latency (mean) | 4.83 s | 31.1 / 100 | lower is better |
| End-to-end latency (p95) | 7.09 s | 42.3 / 100 | lower is better |
| Provider time (mean) | 4.81 s | 31.2 / 100 | lower is better |
| Tool time (mean) | 1.0 ms | 100.0 / 100 | lower is better |
| Framework overhead (mean) | 13.5 ms | 100.0 / 100 | lower is better |
| Framework overhead (p95) | 23.0 ms | 100.0 / 100 | lower is better |
| Framework overhead share | 0.3% | 100.0 / 100 | lower is better |
| Latency per step | 1302.4 ms/step | 61.4 / 100 | lower is better |
| Latency per provider call | 1298.6 ms/call | 57.8 / 100 | lower is better |
| Completion tokens per second | 72.60 tok/s | 100.0 / 100 | higher is better |
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
| Prompt prefix cache hit rate | 55.8% | 93.0 / 100 | higher is better; Predicted share of prompt tokens reusable as a byte-for-byte prefix; this is conservative when tools precede messages. |
| Effective prompt cache hit rate | 83.7% | 100.0 / 100 | higher is better; Provider-reported cache hit rate when available, otherwise the predicted prefix hit rate. |
| Message prefix cache hit rate | 74.0% | 100.0 / 100 | higher is better; Prompt-cache reuse after excluding tool schemas; isolates system-prompt/conversation ordering from tool-catalog churn. |
| Message prefix stability | 92.6% | 100.0 / 100 | higher is better; Prefix retention for system prompt and conversation only, excluding tool schemas. |
| Prompt cache stability | 28.9% | 28.9 / 100 | higher is better; Mean prefix retention penalized by its variation across turns. |
| Stable prefix tokens | 1,230 tokens | 100.0 / 100 | higher is better |
| Cacheable request rate | 80.0% | 100.0 / 100 | higher is better |
| Mean prefix retention | 67.5% | 100.0 / 100 | higher is better |
| Worst prefix retention | 0.4% | 1.5 / 100 | higher is better |
| Tool-schema churn per transition | 40.0% | 60.0 / 100 | lower is better |
| Clock churn per transition | 100.0% | — | lower is better; Clock content changes are expected; what matters is whether the clock is trailing. See trailing rate. |
| Clock in trailing position | 100.0% | 100.0 / 100 | higher is better; Fraction of clock-bearing requests where ## CURRENT TIME is the final message, after the conversation. |
| Identity churn per transition | 0.0% | 100.0 / 100 | lower is better |
| Prefix breaks per run | 2.00 breaks | 60.0 / 100 | lower is better |
| First prompt identical across runs | yes | 100.0 / 100 | higher is better |
| Cache hit-rate variation across runs | 0.6% | 99.4 / 100 | lower is better |
| Reused prompt tokens | 10,688 tokens | — | higher is better |
| Total prompt tokens | 19,157 tokens | — | lower is better |
| Provider-reported cache hit rate | 83.7% | 100.0 / 100 | higher is better |
| Provider-reported cache counters available | yes | — | higher is better |
| Predicted vs reported cache-rate error | 27.9% | 72.1 / 100 | lower is better |

### Cache ablation

| Variant | Hit rate | Stability | Cached tokens | Prompt tokens |
| --- | ---: | ---: | ---: | ---: |
| full | 55.8% | 28.9% | 10688 | 19157 |

**Cache diagnosis:** the clock changes every turn but is trailing, so it no longer invalidates the cached prefix
