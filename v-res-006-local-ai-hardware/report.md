# v-res-006: Local AI Hardware & Compute Landscape (Mid-2026)

**Thesis:** The local AI compute landscape has bifurcated into a NVIDIA CUDA-dominated high-end tier and an Apple-led on-device efficiency tier, with a long tail of specialized ASICs filling edge workloads. The durable moat is shifting from raw FLOPS to integrated software-hardware stacks with strong attestation and power efficiency. For security researchers, this reduces data exfiltration surface but expands firmware and model-weight attack vectors.

**So what?** Local inference lowers cloud dependency and exfiltration risk but requires new detection capabilities for firmware persistence and supply-chain tampering. Power efficiency and attestation are the new primary differentiators.

## Market Structure & Moat Map
- **NVIDIA (dominant high-end):** CUDA ecosystem remains the strongest barrier. Rubin architecture improves efficiency but the software lock-in is the real moat. **Moat:** Durable in training/inference, Transitional in edge.
- **Apple (on-device leader):** MLX framework + unified memory delivers best performance-per-watt for local models. Secure Enclave provides strong attestation. **Moat:** Durable for consumer and enterprise on-device use.
- **AMD, Intel, Google:** Improving but lag in software maturity. **Moat:** Fragile.
- **Specialized ASICs (Groq, Cerebras, Tenstorrent, edge startups):** Extreme efficiency on narrow tasks but poor generalizability. **Moat:** Illusory outside verticals.

## Regulatory & Compliance Risk
Pure local hardware deployment carries minimal regulatory exposure. Primary risks are supply chain provenance (fabrication geography) and firmware-level persistence. No significant new regulations targeting local AI silicon identified in mid-2026 open sources.

## Moat Durability Check
- **Durable:** Software integration (CUDA, MLX) + hardware attestation.
- **Transitional:** Raw compute and memory bandwidth (commoditizing).
- **Fragile/Illusory:** Pure hardware differentiation without ecosystem.

**What to Watch (next 90 days)**
- NVIDIA Rubin Ultra power and efficiency numbers.
- Apple M5 + MLX 2.0 on-device benchmarks.
- Progress on open CUDA alternatives (ROCm maturity).

**Sources (Admiralty graded)**
- NVIDIA technical blogs and earnings (A-1)
- Apple MLX repository and sessions (A-2)
- arXiv papers on edge efficiency (B-2)
- Cross-checked industry benchmarks (C-2)

**Status:** Delivered. Ready for QA.
**Grade received:** Pending.
**GitHub folder:** v-res-006-local-ai-hardware (scrubbed version pushed with this report).

**Options added to root README:**
1. Local Hardware Moat Analysis
2. Gate Architecture for Agentic Systems
3. RAG Optimization for Long-Horizon Research (including attention visualization)