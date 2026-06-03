
# Frontier LLM Field Notes (May 2026)

## Primary Sources

| Tier | Source | URL | Date |
|------|--------|-----|------|
| T1 | OpenAI — Introducing GPT-5 | https://openai.com/index/introducing-gpt-5/ | 2025 (release) |
| T1 | BuildFastWithAI — Best AI Models April 2026 | https://www.buildfastwithai.com/blogs/best-ai-models-april-2026 | 2026-04 |
| T1 | xAI — Grok 3 Announcement | https://x.ai/news/grok-3 | 2025-02 |
| T1 | Google — Gemini 2.5 Pro thinking model | https://blog.google/innovation-and-ai/models-and-research/google-deepmind/gemini-model-thinking-updates-march-2025/ | 2025-03 |
| T1 | Anthropic — Claude Sonnet 4.6 | https://www.anthropic.com/claude/sonnet | 2026-02 |
| T2 | TokenMix — GPT-5.5 Review & Benchmarks | https://tokenmix.ai/blog/gpt-5-5-spud-review-88-swe-bench-2026 | 2026-04 |
| T2 | Llama 4 Developer Guide (Codersera) | https://codersera.com/blog/llama-4-complete-guide-2026/ | 2026-05 |
| T2 | TechCrunch — Grok 3 Release | https://techcrunch.com/2025/02/17/elon-musks-ai-company-xai-releases-its-latest-flagship-ai-grok-3/ | 2025-02 |
| T2 | Artificial Analysis — GPT-5 Benchmarks | https://artificialanalysis.ai/articles/gpt-5-benchmarks-and-analysis | 2025 |
| T2 | o-mega.ai — GPT-5.5 Complete Guide | https://o-mega.ai/articles/gpt-5-5-the-complete-guide-2026 | 2026-04 |
| T2 | Wikipedia — Claude (ongoing) | https://en.wikipedia.org/wiki/Claude_(language_model) | 2026-05 |
| T2 | Multiple — Llama 4 Scout/Maverick specs | Various (listed above) | 2025-2026 |

## Current Frontier Landscape (May 2026)

### The Big Six (Closed Source)

| Model | Lab | Release | SWE-Bench | GPQA Diamond | MMLU | Key Differentiator | Cost (per 1M tokens) |
|-------|-----|---------|-----------|--------------|------|-------------------|---------------------|
| **GPT-5.5 <Spud>** | OpenAI | Apr 2026 | **88.7%** | ~87% | **92.4%** | Best overall frontier; 2× price jump | $5/$30 |
| **Gemini 3.1 Pro** | Google/DeepMind | Mar 2026 | 78.8% | **94.3%** | ~90% | Graduate science leader; 3-hr video context | ~$3.50/$10 |
| **Claude Opus 4.6** | Anthropic | Feb 2026 | **80.8%** | ~88% | ~89% | Real-world coding + agent workflows | ~$15/$75 |
| Claude Sonnet 4.6 | Anthropic | Feb 2026 | ~73% | ~85% | ~86% | Speed/cost balance; "hybrid reasoning" | ~$3/$15 |
| **GPT-5** (w/ reasoning) | OpenAI | All ChatGPT users | ~78% | ~87% | ~90% | Reasoning-effort slider (Min/High) | $2.50/$10 |
| Grok 3 | xAI | Feb 2025 | ~75% | ~82% | ~85% | Chatbot Arena Elo 1402 | ~$2/$10 |

### Open Source That Competes

| Model | Lab | Release | SWE-Bench | Context | Key Differentiator | Cost |
|-------|-----|---------|-----------|---------|-------------------|------|
| **Llama 4 Scout** | Meta | Apr 2025 | ~72% | **10M tokens** (longest open) | MoE, lightweight inference | Free (self-host) |
| Llama 4 Maverick | Meta | Apr 2025 | ~75% | 128K+ | Matches GPT-4o on benchmarks | Free (self-host) |
|| **DeepSeek V4** | DeepSeek | Mar 2026 | ~76% | 256K | 1T params, Ascend chips, no Nvidia | **$0.30/million input** ($0.14/$0.28 Flash) |
| **GLM-5** | Z.ai (Zhipu) | Mar 2026 | **77.8%** | 128K | Chatbot Arena Elo **1451** (top open) | ~$0.40/million |
| Qwen 3.5 | Alibaba | Mar 2026 | ~75% | 128K | 9B active params matching models 13× size | ~$0.15/million |
| MiniMax M2.5 | MiniMax | Mar 2026 | **80.2%** | 200K | Near-closed-source coding performance | ~$1.50/million |

### What Changed in 2026

1. **Cost collapse:** What cost $500/month in 2025 runs for ~$50 today. DeepSeek V3.2 delivers ~90% of GPT-5.4 at 1/50th the price.

2. **Context explosion:** Llama 4 Scout ships with a 10 million-token context window. Enterprise "memory" constraints from 2024 workflows are gone.

3. **Agentic coding as the yardstick:** SWE-bench Verified is now the dominant evaluation (not MMLU). The gap between best-in-class (88.7%, GPT-5.5) and open-source (77.8%, GLM-5) is narrower than ever.

4. **Reasoning-effort sliders:** Models now expose reasoning controls. GPT-5 "Minimal" ~= GPT-4.1 quality; GPT-5 "High" reaches new frontiers with 50–80% fewer output tokens than o3.

5. **Architecture diversification:** Grok runs four parallel agents. GLM-5 uses DeepSeek Sparse Attention. Qwen crams graduate-level reasoning into 9B parameters.

## So What?

1. **The moat is collapsing faster than expected.** Twelve months ago, frontier labs held a clear lead. Now open-source models are 3–10 points behind at 1/100th the cost. This accelerates the viability of local/self-hosted LLMs for commercial products.

2. **Coding agents are the new gold standard.** SWE-bench is the benchmark that matters. If you're evaluating a model for code-heavy workflows, Claude Opus 4.6 and GPT-5.5 are the only serious options. Everything else is a cost/performance tradeoff.

3. **Context is no longer a problem.** 10M tokens (Llama 4 Scout), 3-hour video (Gemini 3.1), 256K+ standard. RAG architectures are being rethought — why chunk when you can ingest the whole corpus?

4. **DeepSeek pricing is market-disruptive.** At $0.30/million input tokens with 76% SWE-bench, DeepSeek V4 undercuts GPT-5 by ~10× while staying within single-digit performance. For price-sensitive products, this is a forcing function.

5. **Viability for a a venture concept:**
   - **Local AI product:** Llama 4 Scout + Qwen 3.5 makes on-device/local-agent products realistic for <$1K hardware.
   - **Code generation SaaS:** The gap between frontier and open-source is narrow enough that a "good enough" coding AI could run at 1/10th the cost with margins VCs like.
   - **Enterprise on-prem:** Anthropic and OpenAI refuse on-prem deployment. Llama 4 + GLM-5 fill this gap for regulated industries.

## Confidence & Caveats

| Claim | Confidence | Caveat |
|-------|------------|--------|
|| GPT-5.5 leads SWE-Bench at ~88.7% (best run) | **High** | Confirmed by multiple T2 sources; typical production range 77–85% |
| Claude Opus 4.6 = best coding agent | **High** | Anthropic's Claude Code workflow achieves 80.9% on SWE-bench — slightly above raw model |
| DeepSeek V4 costs $0.28/million | **Medium** | Pricing volatile; sourced from BuildFastWithAI aggregation |
| Llama 4 10M context is real | **High** | Multiple T2 sources confirm; practical utility at 10M untested |
| Gemini leads GPQA Diamond at 94.3% | **High** | Graduate science benchmark; narrow domain |
| Open-source gap closed to ~3 SWE points | **Medium** | GLM-5 and MiniMax close but not replicated broadly yet |

## Sources Freshness

- GPT-5/GPT-5.5: **Apr 2026** (very recent)
- Gemini 3.1 Pro: **Mar 2026** (recent)
- Claude Opus 4.6: **Feb 2026** (recent)
- Llama 4 Scout/Maverick: **Apr 2025** (stable, widely deployed)
- Grok 3: **Feb 2025** (older; Grok 4 rumored)
- DeepSeek V4/GLM-5/Qwen 3.5: **Mar 2026** (very recent)
- Market analysis: **Apr 2026** (BuildFastWithAI comprehensive)

---
