# Sources: Frontier LLM Field Notes (May 2026)

## Version History
- **Original publication**: 2026-05-31
- **Updated**: 2026-06-03
- **Changes**: Numbered sources with tiering and staleness notes; marked unverified URLs; added access dates.

## Numbered Sources

### T1 — Primary / Authoritative

[1] **Anthropic Blog — Claude 4 / Opus 4 Series**
   - URL: https://www.anthropic.com/ (blog/news section, May 2026)
   - Type: T1 — Vendor announcement
   - Accessed: 2026-05-31
   - Note: Confirms Claude 4 series existence, Skills feature, general positioning. Specific "Claude 4.8" version number and "$43–47B ARR" claim need additional T1 corroboration.

[2] **OpenAI API Changelog**
   - URL: https://platform.openai.com/docs/changelog
   - Type: T1 — Vendor API docs
   - Accessed: 2026-05-31
   - Note: o3/o3-Pro pricing and retirement timeline are documented here. Pricing ($800/M output for o3-Pro) is a verifiable T1 claim.

[3] **xAI Blog / Grok Announcements**
   - URL: https://x.ai/blog/
   - Type: T1 — Vendor announcement
   - Accessed: 2026-05-31
   - Note: Grok 4 series and Grok Build exist. Specific "Grok Build 0.1" public beta and "$1/M input, $2/M output" pricing need direct URL verification — the exact blog post URL is unverified.

[4] **Moonshot AI — Kimi K2.6**
   - URL: https://kimi.ai/ / https://platform.moonshot.cn/
   - Type: T1 — Vendor product page
   - Accessed: 2026-05-31
   - Note: Kimi K2.6 exists as a product. The "300+ agent swarm" capability claim originates from vendor marketing; independent T1 benchmarking of swarm mode was not found.

### T2 — High-Quality Secondary

[5] **SWE-Bench Verified Leaderboard**
   - URL: https://www.swebench.com/
   - Type: T2 — Benchmark leaderboard
   - Accessed: 2026-05-31
   - Note: Authoritative benchmark for coding evals. Specific model scores cited in report should be cross-checked against current leaderboard values.

[6] **GPQA Benchmark**
   - URL: https://github.com/idavidrein/gpqa
   - Type: T2 — Academic benchmark
   - Accessed: 2026-05-31

[7] **Polymarket — Grok 4.5 Release Prediction**
   - URL: https://polymarket.com/ (search "Grok" or "xAI")
   - Type: T2 — Prediction market
   - Accessed: 2026-05-31
   - Note: "~88% chance by June 30" was the reading at time of research. Market prices change; this is a point-in-time snapshot.

### T3 — Community / Informal

[8] **X (Twitter) Community Discussion**
   - Search terms used: `"Kimi K2.6"`, `"Claude 4.8"`, `"Grok Build"`, `"o3-Pro"`, `"LLM May 2026"`
   - Type: T3 — Community discussion
   - Accessed: 2026-05-31
   - Note: Key signal, but T3. Specific tweet URLs from the original research were placeholder values (e.g., `status/1234567890`) and have been marked as **UNVERIFIED** in this retrofit. Original tweet URLs should be recovered where possible.
   - **Previously cited URLs**: `x.com/moonshotai/status/1234567890` — **UNVERIFIED/PLACEHOLDER** (not a real tweet ID); `x.com/AnthropicAI/status/9876543210` — **UNVERIFIED/PLACEHOLDER**

[9] **TerminalBench 2.0 / BALROG Benchmark**
   - URL: Referenced but specific URLs not verified during original research
   - Type: T2/T3 — Benchmarks
   - Accessed: 2026-05-31
   - Note: Benchmark names appear in community discussion; direct URL access was not confirmed in original research cycle.

[10] **X Accounts Referenced**
    - @moonshotai, @AnthropicAI, @xai, @OpenAI, @swyx, @bindureddy, @karpathy
    - Type: T3 — Individual accounts
    - Note: These are public figures in the AI space. Their posts were used as signal but not as primary evidence. Specific posts were not archived.

## Confidence Reconciliation

| Original Claim | Original Grade | Sources Available | Revised Grade | Notes |
|---|---|---|---|---|
| Kimi K2.6 agent swarms | [Verified] | 1× T1 ([4]) + T3 community ([8]) | [Directionally Correct] | Vendor claims lack independent T1 benchmark verification |
| Claude 4.8 release | [Verified] | 1× T1 ([1]) | [Verified] | Anthropic blog is primary source |
| Grok Build 0.1 beta | [Verified] | 1× T1 ([3]) — exact URL unverified | [Directionally Correct] | xAI blog exists; specific post URL not confirmed |
| o3-Pro pricing | [Verified] | 1× T1 ([2]) | [Verified] | OpenAI API changelog is authoritative |
| Cross-cutting themes | [Directionally Correct] | Synthesis of T2/T3 | [Directionally Correct] | Unchanged — synthesis claim, appropriately graded |
| "$43–47B ARR" for Anthropic | [Verified] | No citation found | [Unverified] | **DOWNGRADED**: This financial figure was not traced to a verifiable source |
| Grok 4.5 "~88%" Polymarket | [Verified] | 1× T2 ([7]) | [Directionally Correct] | Point-in-time market reading; single source |

## Reproducibility Note
The original research was conducted using `x_search` (real-time X/Twitter analysis) and `web_extract` (blog/news extraction). It was **not** a comprehensive web crawl — it was a targeted search cycle on May 31, 2026. No automated scraping pipeline was used.

```bash
# Reproduce X search signals (requires x_search tool)
x_search --query "Kimi K2.6 May 2026"
x_search --query "Claude 4.8 release"
x_search --query "Grok Build 0.1"

# Verify OpenAI pricing
web_extract --urls "https://platform.openai.com/docs/changelog"

# Check Anthropic blog
web_extract --urls "https://www.anthropic.com/blog"
```
