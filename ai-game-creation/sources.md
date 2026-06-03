# Sources: AI Game Creation (2026)

## Version History
- **Original publication**: 2026-05-31
- **Updated**: 2026-06-03
- **Changes**: Numbered sources with tiering; marked all placeholder/fabricated URLs; added access dates; reconciled confidence.

## Numbered Sources

### T1 — Primary / Authoritative

[1] **Claude Code Game Studios — GitHub Repository**
   - URL: https://github.com/donchitos/claude-code-game-studios
   - Type: T1 — Open-source project
   - Accessed: 2026-05-31
   - Note: Repository exists. Claims about 48–49 agent hierarchy, 70+ slash commands, and engine-specific sets can be verified by inspecting the repo. MIT license.

[2] **xAI Blog — Grok Announcements**
   - URL: https://x.ai/blog/
   - Type: T1 — Vendor blog
   - Accessed: 2026-05-31
   - Note: Grok Imagine and Grok Build features are announced here. Specific "grok-imagine" blog post URL not individually confirmed. The "fully AI-generated game by end of 2026" goal is a vendor marketing statement.

[3] **Moonshot AI — Kimi K2.6**
   - URL: https://kimi.ai/ / https://platform.moonshot.cn/
   - Type: T1 — Vendor product page
   - Accessed: 2026-05-31
   - Note: Kimi K2.6 exists. "300+ parallel agents" is a vendor claim.

### T2 — High-Quality Secondary

[4] **Godot Engine Documentation**
   - URL: https://docs.godotengine.org/
   - Type: T1/T2 — Open-source engine docs
   - Accessed: 2026-05-31
   - Note: Referenced in context of Claude Code Game Studios supporting Godot 4.

### T3 — Community / Informal

[5] **X (Twitter) Community Discussion**
   - Search terms: `"AI game creation"`, `"agentic game dev"`, `"Claude game studio"`, `"Kimi swarm game"`
   - Type: T3 — Community discussion
   - Accessed: 2026-05-31
   - **⚠️ Previously cited URLs**: `x.com/moonshotai/status/1234567890` — **UNVERIFIED/PLACEHOLDER**; `x.com/xai/status/9876543210` — **UNVERIFIED/PLACEHOLDER**

[6] **X Accounts Referenced**
   - @donchitos, @moonshotai, @xai, @AnthropicAI, @godotengine, @unity3d
   - Type: T3 — Individual/org accounts
   - Note: Public accounts. Specific posts not archived.

### UNSUPPORTED — Marked in Retrofit

[7] **Medium: "AI Game Dev with Kimi Swarms"**
   - URL: `medium.com/@ai-gamedev/kimi-swarms-2026`
   - **Status: UNVERIFIED** — Medium article URL not confirmed as a real, accessible page.

[8] **Medium: "Kimi Swarm VRAM Requirements"**
   - URL: `medium.com/@ai-hardware/kimi-swarm-vram-2026`
   - **Status: UNVERIFIED** — Medium article URL not confirmed.

[9] **xAI Benchmarks Page**
   - URL: `x.ai/benchmarks/grok-imagine`
   - **Status: UNVERIFIED** — Specific benchmark URL not confirmed.

## Confidence Reconciliation

| Original Claim | Original Grade | Revised Grade | Justification |
|---|---|---|---|
| Claude Code Game Studios (48–49 agents, 70+ commands) | [Verified] | [Verified] | GitHub repo [1] exists and can be inspected |
| Kimi K2.6 300+ parallel agents | [Verified] | [Directionally Correct] | Vendor claim [3]; independent verification limited |
| Grok Imagine on-the-fly assets | [Verified] | [Directionally Correct] | xAI blog [2] exists; specific post not confirmed |
| Grok "fully AI game by 2026" | [Verified] | [Directionally Correct] | Vendor marketing statement [2] |
| Hardware: 24GB+ VRAM for Kimi swarms | [Verified] | [Unverified] | **DOWNGRADED**: Source [8] is unverified Medium article; no T1/T2 benchmark found |
| Workflow hybrid (Claude+Kimi+Grok) | [Directionally Correct] | [Directionally Correct] | Synthesis claim, appropriately graded |

## Reproducibility Note
Research was conducted using `x_search` and browser inspection of the GitHub repo. It was **manual**, not automated.

```bash
# Inspect Claude Code Game Studios
gh repo clone donchitos/claude-code-game-studios
cd claude-code-game-studios
ls -la

# Search X for community reports
x_search --query "AI game creation agentic 2026"
x_search --query "Claude game studio"

# Check Grok announcements
web_extract --urls "https://x.ai/blog/"
```
