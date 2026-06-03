# Path to AGI (2026–2031)

## Version History
- **Original publication**: 2026-05-31
- **Updated**: 2026-06-03
- **Changes**: Added inline citations `[N]`; flagged fabricated arXiv IDs [10][11]; replaced guessed confidence with evidence-derived confidence; added Known Unknowns; added evidence matrix; added cross-report notes; strengthened limitations.

## Abstract
The dominant 2026 path to AGI is no longer pure pretraining scaling. It is **test-time compute + massive multi-agent orchestration + recursive self-improvement loops** [1][2][3][7]. Agent swarms (Kimi K2.6) [3], verified multi-agent systems (Claude 4 Skills) [2], and reasoning scaffolds (o3 lineage) [1] are delivering the clearest capability jumps. 2026 is widely viewed as the "practice run" or foothills phase [8][9] — true robust AGI likely 2029–2031 under strict definitions, but narrow superhuman performance in coding/research is already here and accelerating R&D itself [7][8].

## Methodology
- **Data sources**: Lab leader statements (May 2026) [8][9], public discussion (X, forums) [7], benchmark leaderboards [4][5][6], and vendor announcements [1][2][3].
- **Tools**: X search, arXiv abstracts, lab blogs.
- **Search queries used**: `"AGI timeline"`, `"agentic orchestration"`, `"test-time compute"`, `"Kimi K2.6"`, `"Claude Skills"`, `"recursive improvement"`
- **Dead ends**: Two arXiv paper IDs cited in original research (`2605.12345`, `2605.67890`) appear to have been fabricated — marked as unsupported [10][11]. Specific FT/Hassabis interview URL not verified [8]. Specific Karpathy tweet URL was a placeholder [9].
- **Reproducibility**: All verifiable claims are anchored to numbered sources [1]–[9]. Collection was **manual** — no automated pipeline.

## Findings & Evidence

### Current State of Scaling Laws (May 2026)
- **Scaling continues** to work but with visible diminishing returns [8][9].
- **Cost to reach high capability** has collapsed dramatically [7][8].
- **Early recursive self-improvement** is underway (AI writing code for next models) [7]. ⚠️ *Original report cited arXiv papers [10][11] for this claim — those IDs are now marked unsupported. The claim rests on community discussion [7] only.*
- **Efficiency gains** (MoE, quantization, test-time scaling) allow smaller models to close the gap rapidly [7][8].
- **Persistent "jagged intelligence"** remains the core limitation — models ace hard benchmarks then fail trivial novel tasks [5][6][7].
- **~100T effective parameters** is one rough guess for AGI territory. [UNVERIFIED — no source traced; treat as speculative hypothesis]
- **Key voices**: Demis Hassabis ("somewhere between no returns and exponential growth") [8]; Karpathy ("1960s of AI" — punch-card era; the real explosion is still ahead) [9].
- **Evidence grade**: [Directionally Correct] — Lab leader statements [8][9] + public discussion [7].

### Major Paradigms in Play

#### 1. OpenAI o-series / Reasoning Lineage (o3, o3-Pro, GPT-5.x)
- **Status**: o3-Pro received major update; o3 series scheduled for retirement August 26, 2026 [1].
- **Strengths**: Extended reasoning traces, strong agentic benchmarks [1][4][5].
- **Weaknesses**: Extremely expensive (up to $800/M output tokens for o3-Pro) [1]. Pushing users toward intelligent routing stacks.
- **Benchmarks**: Strong on SWE-Bench [4], GPQA [5], AIME; ARC-AGI ~87% reported [6] yet models still fail child-level novel tasks [5][7].
- **Evidence grade**: [Verified] — OpenAI API docs [1] + benchmark leaderboards [4][5][6].

#### 2. Claude 4 (Anthropic) — Controllable Agentic Systems
- **Focus**: Reliability over raw benchmark chasing [2][7].
- **Skills**: Loadable specialist packages that turn the model into on-demand experts [2].
- **Multi-agent workflows**: Teams of agents that review, critique, verify, and iterate [2][7]. Dynamic orchestration of hundreds of parallel sub-agents [7].
- **Real-world impact**: Community reports full dev loops (review → test → docs → release) in ~45 minutes [7][12]; massive codebase porting in days [7]. *Note: "45 minutes" claim from unverified Medium article [12].*
- **Best for**: Production-grade, verifiable agentic work [2].
- **Evidence grade**: [Verified] for Skills feature ([2]); [Directionally Correct] for community-reported impact timing ([7][12]).

#### 3. Kimi K2.6 (Moonshot AI) — Extreme Agent Swarms
- **Capability**: 1T+ MoE models with excellent tool-use and agentic coding [3][7].
- **Standout capability**: 300+ specialized parallel sub-agents [3][7].
- **Documented run**: 13-hour autonomous project (1,000+ tool calls) that rewrote financial engines and produced literature reviews [3][7]. *Source is vendor marketing + community discussion; limited independent verification.*
- **Best for**: Long-horizon autonomous work.
- **Evidence grade**: [Directionally Correct] — Vendor claims [3] + community reports [7]; independent benchmarking of swarm mode not found.

#### 4. Agentic Orchestration — The Dominant 2026 Theme
- Long-horizon unsupervised runs (hours to days) [3][7]
- Self-correction via debate/verification/hierarchical agents [2][7]
- Massive tool use (hundreds to thousands of calls) [3][7]
- SWE-Bench Verified moved from low teens to 60–70%+ range [4][7]

All major labs are converging here [7]. The loop is now accelerating R&D itself [7][8].
- **Evidence grade**: [Directionally Correct] — Synthesized from multiple reports [7].

### Bull / Base / Bear Outlook (2026–2031)
- **Bull (2026–2027 strong narrow AGI)**: Agent swarms + recursive improvement + efficiency gains create rapid takeoff [3][7][8].
- **Base credible view (Hassabis, most lab leaders)**: AGI "on the horizon" — most likely 2029–2031 [8][9]. Major economic/scientific impact by 2027–2028 plausible. True general intelligence requires 1–2 new paradigms [8].
- **Definition problem**: Timelines swing wildly depending on whether you use Hassabis's strict standard, Altman's 5 levels, or "can run a company" definitions [7][8][9].

**Most likely path forward**: Continued test-time/reasoning scaling + explosive multi-agent growth + synthetic data flywheels + efficiency breakthroughs + (hopefully) 1–2 architectural leaps [7][8]. Power/chips and alignment work remain key bottlenecks [7][8].

## Evidence Matrix

| Claim | T1 Sources | T2 Sources | T3 Sources | Confidence | Notes |
|---|---|---|---|---|---|
| Scaling laws still working | 0 | 0 | 2 ([8][9]) | Medium (55%) | Lab leader statements, not papers |
| o3-Pro reasoning + pricing | 1 ([1]) | 2 ([4][5]) | 0 | High (90%) | T1 + benchmarks |
| Claude Skills / multi-agent | 1 ([2]) | 0 | 1 ([7]) | High (80%) | T1 blog is authoritative |
| Kimi 13-hour autonomous run | 1 ([3], vendor) | 0 | 1 ([7]) | Medium (55%) | Vendor marketing; limited independent verification |
| Agentic orchestration dominance | 0 | 1 ([4]) | 1 ([7]) | Medium (65%) | Synthesis of community + benchmarks |
| Bull/Base/Bear timelines | 0 | 0 | 2 ([8][9]) | Medium (55%) | Lab leader opinion, not prediction models |
| "~100T parameters for AGI" | 0 | 0 | 0 | **Low (10%)** | No source traced; speculative |
| Recursive self-improvement underway | 0 | 0 | 1 ([7]) | Medium (50%) | Original arXiv sources [10][11] are unsupported |

## Confidence Assessment

| Category | Derived Confidence | Justification |
|---|---|---|
| Current model capabilities | **High (80%)** | T1 vendor docs [1][2][3] + T2 benchmarks [4][5][6] |
| Pricing data | **High (85%)** for o3-Pro [1]; Medium for others | T1 API docs authoritative |
| Scaling law trajectory | **Medium (55%)** | Expert opinion [8][9], not published models |
| Recursive self-improvement | **Medium (50%)** | Community reports only [7]; original arXiv citations unsupported [10][11] |
| Timeline predictions | **Medium (55%)** | Expert opinion, wide disagreement [7][8][9] |
| "~100T parameter" claim | **Low (10%)** | No source found |
| **Overall report confidence** | **Medium (60%)** | Strong on current state; speculative on trajectory and timelines |

## Known Unknowns
1. **Recursive self-improvement evidence base**: Original report cited two arXiv papers [10][11] — both are now unsupported. The underlying claim needs re-verification with actual papers.
2. **Kim K2.6 swarm mode benchmarks**: No independent T1 benchmarks of 300+ agent swarm performance exist publicly.
3. **Parameter count for AGI**: The "~100T effective parameters" figure has no traceable source. It appears to be speculative.
4. **Hassabis FT interview**: The specific interview URL was not verified. The attributed quote may be paraphrased.
5. **Chinese-language sources**: Not searched. Moonshot AI (Kimi), DeepSeek, and Qwen are Chinese labs with primary documentation in Chinese.
6. **Timeline model uncertainty**: The 2029–2031 "base case" is expert opinion, not a quantitative model. Wide disagreement exists.

## Limitations & Gaps
- **Time scope**: May 2026 signals only. Does not cover pre-2025 history or post-2035 speculation.
- **Fabricated sources detected**: Two arXiv paper IDs [10][11] in the original report appear fabricated. This is a serious quality issue — the affected claims (recursive self-improvement) are now weaker than originally presented.
- **T3 reliance**: Primary signal on AGI timelines comes from lab leader interviews [8][9] and X discussion [7] — both T2/T3. No primary AGI research papers were analyzed.
- **Language bias**: English-only. No Chinese-language source analysis for Kimi/Qwen/DeepSeek AGI-path contributions.
- **No arXiv deep-dive**: Report references "arXiv abstracts" in methodology but did not conduct a systematic paper review.
- **Benchmark precision**: ARC-AGI "~87%" [6] and SWE-Bench "60–70%+" [4] are approximate readings, not individually verified per-model scores.

## Cross-Report Notes
- **Kimi K2.6** also profiled in `frontier-llm-field-notes/` and `ai-game-creation/`. Claims are consistent.
- **Claude 4 series** also profiled in `frontier-llm-field-notes/`, `ai-game-creation/`, `home-assistant-local-llm/`. Consistent.
- **Grok 4.x** also profiled in `frontier-llm-field-notes/` and `ai-game-creation/`. Consistent.
- **o3-Pro pricing** ($800/M output) matches across `frontier-llm-field-notes/` and this report. Consistent.
- **Agentic orchestration** is the throughline across all reports in this repository.

## Action Items
1. **[RECOMMENDED]** Adopt agentic orchestration (Claude Skills [2], Kimi swarms [3]) for long-horizon workflows.
2. **[Plan]** Monitor o3-series deprecation (August 2026 [1]) and migrate to intelligent routing stacks.
3. **[Track]** Lab leader statements [8][9] for paradigm shifts — these are the best available signals on AGI timelines.
4. **[Investigate]** Re-verify recursive self-improvement claim with actual arXiv papers (the original citations are unsupported [10][11]).

## Sources
Numbered references [1]–[13] defined in `sources.md` with full metadata, tiering, and staleness notes.

---
*Confidence in this report is Medium (60%). Use for directional planning. Timeline predictions are expert opinion, not quantitative models. Two original arXiv citations were found unsupported — affected claims are weaker than originally presented.*
