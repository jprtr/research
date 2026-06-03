# Sources

## Version History
- **Original**: 2026-05-31
- **Updated**: 2026-06-03 (T1 sources verified per Vanguard Research Directive)

## Tier 1 Sources (Primary Evidence)

### Game Engine AI Documentation

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| Unity ML-Agents manual | https://docs.unity3d.com/Packages/com.unity.ml-agents@3.0/manual/index.html | T1 — Engine docs | Primary documentation for training agents in Unity environments |
| HuggingFace Deep RL course — Unit 5 (Unity ML-Agents) | https://huggingface.co/learn/deep-rl-course/unit5/introduction | T1/T2 — Educational | Educational source for RL in game environments; not equal to engine-owner docs but provides worked examples |

### Open-Source Frameworks (Verified)

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| Claude Code Game Studios | https://github.com/donchitos/claude-code-game-studios | T1 — Code repository | Verified GitHub repo with 48–49 agent org hierarchy and 70+ slash commands |

## Tier 1 Validation Notes

- **Claude Code Game Studios**: GitHub repo verified — MIT licensed, active codebase. Claims about agent hierarchy and command count can be verified by inspecting the repo directly.
- **Unity ML-Agents**: Official Unity documentation, actively maintained with version-specific URL.
- **HuggingFace course**: Quality educational resource; demonstrates practical RL-in-games workflows but is not an engine-owner source.

### Critical Source Corrections

- **Fabricated X/Twitter URLs**: `x.com/xai/status/9876543210` and `x.com/moonshotai/status/1234567890` — removed from sources. These were placeholder URLs that do not resolve to real tweets.
- **Fabricated Medium URLs**: `medium.com/@ai-gamedev/kimi-swarms-2026` and `medium.com/@ai-hardware/kimi-swarm-vram-2026` — marked as UNVERIFIED. These URLs were not confirmed as real, accessible pages.
- **Grok Imagine claims**: The original report referenced "xAI Blog — Grok Imagine" (https://x.ai/blog/grok-imagine) — this specific URL was not confirmed as a real page. Grok features are discussed generally but this T1 source needs re-verification.
- **Hardware VRAM requirements**: Original report claimed "24GB+ VRAM for 300+ Kimi swarms" citing only an unverified Medium post [8]. This claim has been downgraded to **[Unverified]** pending independent evidence.

## Tier 2 Sources (Supplemental Context)

| Source | Type | Note |
|--------|------|------|
| xAI blog (https://x.ai/blog/) | T1 — Vendor blog | Grok general announcements; specific post URLs not individually confirmed |
| Moonshot AI (https://www.moonshot.ai) | T1 — Vendor page | Kimi product positioning |
| Kimi K2.6 HuggingFace card | T1 — Model card | Weights and metadata |

## Tier 3 Sources (Community Context)

| Source | Type | Note |
|--------|------|------|
| X account @donchitos | T3 | Creator of Claude Code Game Studios |
| X accounts @moonshotai, @xai, @AnthropicAI | T3 | Vendor social accounts — signal, not evidence |

## Source Quality Policy

Per the Vanguard Research Directive:
- T1 sources (Unity docs, GitHub repos, HuggingFace) are the foundation for all game AI and framework claims
- T2 sources (vendor blogs, product pages) provide direction context but not evidence for specific capabilities
- T3 sources (X/Twitter, community reports) are discovery tools only
- Claims about Kimi swarm capabilities, Grok Imagine, and hardware requirements need stronger T1/T2 evidence
- Every URL must be opened and validated before citation
- Fabricated or unverified Medium/URL sources have been flagged and claims resting solely on them have been downgraded
