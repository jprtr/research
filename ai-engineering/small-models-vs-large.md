---
pillar: AI Engineering
type: single
---

Small models beating large ones isn't a myth, but it's conditional. Three verified cases, one fake claim, and the architecture that makes it reproducible.

**When it works:**
1. The task is bounded (classification, extraction, re-ranking).
2. The small model is fine-tuned on the specific output distribution of a larger teacher.
3. Inference uses constrained decoding or sparse activation, not dense brute force.

**Case 1: Qwen3-4B fine-tuned vs 120B teacher**
DistiLabs benchmark, Dec 2025. The 4B model matched the 120B teacher on 7 of 8 benchmarks and beat it by 19 points on SQuAD 2.0. The trick wasn't architecture — it was distilling the teacher's output distribution onto a single task.

**Case 2: Liquid AI LFM2.5-8B-A1B on-device**
8.3B total parameters, 1.5B active MoE, 128K context. Demoed running 67 tools across 13 MCP servers locally with sub-second dispatch. The win isn't quality — it's latency and zero data exfiltration. Vendor-reported demo, not independently benchmarked.

**Case 3: Mixtral 8x7B vs Llama 2 70B**
~13B active parameters, 46.7B total. Matched or beat Llama 2 70B and GPT-3.5 across most benchmarks at 6x inference speed. Sparse MoE: 2 experts per token. Same quality, less compute per forward pass.

**What I couldn't verify:**
A claim that Phi-4 (14B) beats GPT-4o on math/reasoning. Source conflated two separate announcements. Independent corroboration not found. Treat as speculation.

**The production architecture: Small-First Routing**
Route everything to the small model first. Quality-check the output. Escalate to frontier only on low confidence.

| Workload | Blended Cost | Escalation Rate |
|---|---|---|
| Classification / Extraction | ~2-5% of frontier | 1-5% |
| RAG re-ranking | ~2% of frontier | 1-5% |
| Summarization | ~20% of frontier | 1-5% |
| Open-ended reasoning | ~30% of frontier | 15-30% |
| Code generation | ~30% of frontier | 15-30% |

At 70% SLM / 30% frontier, blended cost ≈ 1/3 of pure frontier. p50 latency 5-10x faster on the majority of requests.

**The stack**
- Serving: vLLM with continuous batching and PagedAttention.
- Fine-tuning: QLoRA (4-bit base + LoRA adapters) on 3 months of production inputs/outputs.
- Hardware: ~24GB VRAM (RTX 4090, A10G, L4 class).
- Metric to watch: Escalation rate. If it's >10% on classification tasks, your SLM isn't fine-tuned enough.

**Where small models still lose**
1. Open-ended reasoning across diverse domains.
2. Multi-file code architecture (>500 lines).
3. Complex multi-step agent planning.

Use frontier models for planning, SLMs for execution. Hybrid is the only honest architecture right now.
