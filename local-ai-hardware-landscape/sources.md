# Sources

## Version History
- **Original**: 2026-06-01
- **Updated**: 2026-06-03 (T1 sources verified per Vanguard Research Directive)

## Tier 1 Sources (Primary Evidence)

### NVIDIA Hardware

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| NVIDIA Jetson Orin family | https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/jetson-orin/ | T1 — Vendor specs | Official edge hardware specs and product positioning |
| NVIDIA NemoClaw product page | https://www.nvidia.com/en-us/ai/nemoclaw/ | T1 — Vendor page | Official architecture positioning for local AI |
| NVIDIA Build: NemoClaw on Spark | https://build.nvidia.com/spark/nemoclaw | T1 — Setup guide | Official guided setup for DGX Spark |

### Apple

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| Apple MLX | https://github.com/ml-explore/mlx | T1 — Code repository | Official Apple local inference framework source |

### Open Inference Runtimes

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| llama.cpp | https://github.com/ggerganov/llama.cpp | T1 — Code repository | Primary open-source inference runtime |
| Ollama | https://ollama.ai/ | T1 — Vendor page | Official model serving stack source |

### Qualcomm

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| Qualcomm AI platform | https://www.qualcomm.com/artificial-intelligence | T1 — Vendor page | Official Qualcomm AI stack and NPU positioning source |

### Regulatory Context

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| EU AI Act compliance | https://www.specira.ai/ (referenced as Specira) | T2 — Regulatory analysis | EU AI Act risk classification framework |

## Tier 1 Validation Notes

- **URLs verified on 2026-06-03**: All T1 URLs above were accessed and confirmed to match the claims they support
- **Official vendor spec pages**: NVIDIA, Apple, Qualcomm claims are grounded in official product documentation
- **Code repositories**: llama.cpp, MLX, and Ollama are real, actively maintained, and the primary sources for inference capabilities
- **Source shift**: Prior version of this report referenced "compute-market.com benchmarks," "pooyagolchian.com," "heyuan110.com," "modelfit.io," "todaypeek.com," "newegg.com" — these are T2/T3 at best. Claims originally attributed to those sources should be treated as provisional unless also supported by T1 vendor docs or code repos.

## Tier 2 Sources (Supplemental Context Only)

The following T2/T3 sources were used in the original report for market context but are **not** used as primary evidence for capability or performance claims:

| Source | Type | Note |
|--------|------|------|
| presenc.ai | T2 — Market research | NVIDIA market share estimates |
| introl.com | T2 — Technical analysis | CUDA moat analysis |
| spheron.network | T2 — Technical comparison | ROCm vs CUDA 2026 |
| compute-market.com | T2 — Benchmarks | MLX vs llama.cpp |
| opensourceforu.com | T2 — Product review | Tenstorrent TT-QuietBox |
| voiceflow.com | T2 — Product analysis | Groq 2026 |

**Source quality note**: Vendor spec pages (T1) should be the primary basis for TOPS, pricing, and capability claims. T2 benchmark blogs are useful supplementary evidence but not sufficient alone.

## Source Quality Policy

Per the Vanguard Research Directive:
- T1 sources (vendor official, code repos, standards docs) are the foundation for all hardware capability and performance claims
- T2 sources (tech journalism, benchmark blogs) provide market context and competitive comparisons
- T3 sources (Reddit, forums, social media) are discovery tools and sentiment indicators only
- Claims originally sourced from T2/T3 benchmark sites should be re-verified against T1 vendor pages where possible
- Pricing claims are point-in-time and should be treated as dated snapshots
- Every URL must be opened and validated before citation
