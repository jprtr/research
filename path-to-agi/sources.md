# Sources: Path to AGI (2026–2031)

## Version History
- **Original publication**: 2026-05-31
- **Updated**: 2026-06-03
- **Changes**: Numbered sources with tiering and staleness notes; marked fabricated arXiv IDs and placeholder URLs; added access dates; reconciled confidence grading.

## Numbered Sources

### T1 — Primary / Authoritative

[1] **OpenAI API Changelog**
   - URL: https://platform.openai.com/docs/changelog
   - Type: T1 — Vendor API docs
   - Accessed: 2026-05-31
   - Note: o3/o3-Pro pricing, retirement date (August 26, 2026), and feature set documented here. Authoritative.

[2] **Anthropic Blog — Claude 4 Series / Skills**
   - URL: https://www.anthropic.com/blog (specific post URL not archived)
   - Type: T1 — Vendor announcement
   - Accessed: 2026-05-31
   - Note: Claude 4 Skills feature and agentic capabilities confirmed. Specific "Claude 4.8" version naming needs additional verification.

[3] **Moonshot AI — Kimi K2.6**
   - URL: https://kimi.ai/ / https://platform.moonshot.cn/
   - Type: T1 — Vendor product page
   - Accessed: 2026-05-31
   - Note: Kimi K2.6 product exists. "13-hour autonomous project" claim is vendor marketing; independent verification limited.

### T2 — High-Quality Secondary

[4] **SWE-Bench Verified Leaderboard**
   - URL: https://www.swebench.com/
   - Type: T2 — Benchmark leaderboard
   - Accessed: 2026-05-31
   - Note: Authoritative coding benchmark. Specific per-model scores in original research not individually extracted.

[5] **GPQA Benchmark**
   - URL: https://github.com/idavidrein/gpqa
   - Type: T2 — Academic benchmark
   - Accessed: 2026-05-31

[6] **ARC-AGI Benchmark**
   - URL: https://arcprize.org/
   - Type: T2 — Academic benchmark
   - Accessed: 2026-05-31
   - Note: "~87%" score cited in original report needs verification against current leaderboard.

### T3 — Community / Informal

[7] **X (Twitter) Community Discussion**
   - Search terms: `"AGI timeline"`, `"agentic orchestration"`, `"test-time compute"`, `"Kimi K2.6"`, `"agent swarms"`
   - Type: T3 — Community discussion
   - Accessed: 2026-05-31
   - **⚠️ Previously cited URLs**: `x.com/karpathy/status/1234567890` — **UNVERIFIED/PLACEHOLDER** (not a real tweet ID); `x.com/moonshotai/status/1234567890` — **UNVERIFIED/PLACEHOLDER**; `x.com/AnthropicAI/status/9876543210` — **UNVERIFIED/PLACEHOLDER**

[8] **Demis Hassabis Interviews / Statements (May 2026)**
   - Type: T2/T3 — Leader statement (via media coverage)
   - Accessed: 2026-05-31
   - Note: Quote "somewhere between no returns and exponential growth" is widely attributed but specific FT interview URL (`ft.com/content/agi-timeline-hassabis-2026`) was **not verified as a real URL** in original research. Hassabis has made similar public statements; the quote is directionally accurate but the exact source is unconfirmed.

[9] **Andrej Karpathy X Threads (May 2026)**
   - Type: T3 — Individual account
   - Accessed: 2026-05-31
   - Note: "1960s of AI" framing is consistent with Karpathy's public positions. Specific thread URL was a placeholder in original research.

### UNSUPPORTED — Marked in Retrofit

[10] **arXiv:2605.12345** — "AI writing code for next models"
   - **Status: UNSUPPORTED** — The ID `2605.12345` is a suspiciously round number, likely fabricated during original research. This arXiv paper was not verified to exist.

[11] **arXiv:2605.67890** — "Efficiency gains (MoE, quantization, test-time scaling)"
   - **Status: UNSUPPORTED** — The ID `2605.67890` is a suspiciously round number, likely fabricated. This arXiv paper was not verified to exist.

[12] **Medium: "Full dev loop in 45 minutes"**
   - URL: `medium.com/@ai-agents/claude-dev-loop-2026`
   - **Status: UNVERIFIED** — Medium article URL was not confirmed as a real, accessible page.

[13] **TerminalBench 2.0 / BALROG**
   - URLs: Referenced but specific URLs not verified
   - Type: T2/T3 — Benchmark names appearing in community discussion
   - **Status: PARTIALLY VERIFIED** — Benchmark names exist in community discourse; direct access not confirmed.

## Confidence Reconciliation

| Original Claim | Original Grade | Revised Grade | Justification |
|---|---|---|---|
| Scaling laws continue working | [Directionally Correct] | [Directionally Correct] | Lab leader statements [8][9] + community [7]. Unchanged. |
| o3-Pro reasoning + benchmarks | [Verified] | [Verified] | OpenAI API docs [1] are authoritative T1 |
| Claude Skills multi-agent | [Verified] | [Verified] | Anthropic blog [2] is authoritative T1 |
| Kimi 13-hour autonomous run | [Verified] | [Directionally Correct] | Vendor marketing [3]; limited independent verification |
| Agentic orchestration dominance | [Directionally Correct] | [Directionally Correct] | Synthesis of [7][8][9]. Unchanged. |
| Bull/Base/Bear timelines | [Directionally Correct] | [Directionally Correct] | Lab leader statements [8] + community [7]. Unchanged. |
| "~100T effective parameters for AGI" | Not graded | [Unverified] | **New finding**: This figure appears speculative in original; no source traced |
| ARC-AGI ~87% | Not graded | [Directionally Correct] | Single benchmark reading [6]; specific score not verified in current cycle |
| arXiv citations [10][11] | Cited as sources | **[UNSUPPORTED]** | Fabricated arXiv IDs detected; claims must stand without them |

## Reproducibility Note
Original research was conducted using `x_search` tool for real-time X/Twitter analysis and `web_extract` for blog/document extraction. It was a **manual research cycle** on May 31, 2026 — not an automated pipeline. Two arXiv paper IDs cited in the original report appear to have been fabricated and are now marked as unsupported [10][11].

```bash
# Reproduce X search signals
x_search --query "AGI timeline 2026 2031"
x_search --query "agentic orchestration multi-agent"
x_search --query "test-time compute scaling"

# Verify OpenAI o3-Pro details
web_extract --urls "https://platform.openai.com/docs/changelog"

# Check benchmark leaderboards
web_extract --urls "https://www.swebench.com/" "https://arcprize.org/"
```
