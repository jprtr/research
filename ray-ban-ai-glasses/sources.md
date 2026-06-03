# Sources: Meta Ray-Ban AI Glasses Teardown (2026)

## Version History
- **Original publication**: 2026-05-31
- **Updated**: 2026-06-03
- **Changes**: Numbered sources with tiering; marked ALL URLs as needing verification (original iFixit/FCC/Bloomberg/Meta blog URLs were not confirmed as real pages); flagged contradiction with `meta-ray-ban-ai-glasses/` report; reconciled confidence to evidence base.

## Numbered Sources

### T1 — Primary / Authoritative

[1] **iFixit Teardown — Ray-Ban Meta**
   - Originally cited URL: `https://www.ifixit.com/Teardown/Meta+Ray-Ban+AI+Glasses+2026`
   - **Status: URL UNVERIFIED** — This specific URL was not confirmed as a real, accessible page during original research or retrofit.
   - **Alternative verified source**: iFixit has published Ray-Ban Meta teardowns (confirmed via general iFixit catalog). The `meta-ray-ban-ai-glasses/` report in this repo cites a real iFixit URL: https://www.ifixit.com/News/113543/theres-groundbreaking-waveguide-tech-inside-metas-800-ar-glasses-but-dont-count-on-fixing-them (Oct 2025, verified).
   - Type: T1 — Teardown documentation
   - Accessed: 2026-05-31

[2] **Meta Engineering Blog — Multimodal AI for Ray-Ban Meta**
   - URL: https://engineering.fb.com/2025/03/04/virtual-reality/building-multimodal-ai-for-ray-ban-meta-glasses/
   - Type: T1 — Engineering blog
   - Accessed: 2026-05-31 (referenced from `meta-ray-ban-ai-glasses/` report which verified this URL)
   - Note: Authoritative on architecture. **Key finding**: Confirms multimodal AI is cloud-processed, not on-device.

[3] **Meta Blog — Ray-Ban AI Edition**
   - Originally cited URL: `https://about.fb.com/news/2026/05/ray-ban-ai-glasses`
   - **Status: URL UNVERIFIED** — This specific URL was not confirmed. Meta's about.fb.com hosts real announcements but the exact slug needs verification.
   - Type: T1 — Vendor announcement

[4] **FCC Filings — Ray-Ban Meta**
   - Originally cited URL: `https://fccid.io/2AHRD-RAYBAN2026`
   - **Status: URL UNVERIFIED** — FCC ID format looks plausible but the specific ID was not confirmed.
   - Type: T1 — Regulatory filing

[5] **Qualcomm Snapdragon AR1+ Gen 1**
   - Reference (verified from `meta-ray-ban-ai-glasses/`): https://9to5google.com/2025/06/10/snapdragon-ar1-gen-1/
   - Type: T2 — Tech news
   - Accessed: 2026-05 (per `meta-ray-ban-ai-glasses/`)
   - Note: Qualcomm explicitly advertises "NPU can run small language models on-device" for AR1+ Gen 1 — implying current AR1 Gen 1 cannot.

[6] **Meta Ray-Ban Privacy Policy**
   - Originally cited URL: `https://www.meta.com/legal/ray-ban-privacy-policy`
   - **Status: PLAUSIBLE** — Meta's legal pages exist at this domain, but exact URL structure may vary.
   - Type: T1 — Legal documentation

### T2 — High-Quality Secondary

[7] **Wikipedia — Ray-Ban Meta**
   - URL: https://en.wikipedia.org/wiki/Ray-Ban_Meta
   - Type: T2 — Encyclopedic
   - Accessed: 2026-05 (per `meta-ray-ban-ai-glasses/`)
   - Note: Baseline specs confirmed across sources.

[8] **Tom's Guide Review**
   - URL: https://www.tomsguide.com/reviews/ray-ban-meta-smart-glasses
   - Type: T2 — Product review
   - Accessed: 2024 (per `meta-ray-ban-ai-glasses/`)
   - Note: Storage + battery data. Dated (2024) — may not reflect 2026 model.

### T3 — Community / Informal

[9] **X (Twitter) Community Discussion**
   - Search terms: `"Ray-Ban AI glasses"`, `"Meta smart glasses"`, `"Ray-Ban AI teardown"`
   - Type: T3 — Community discussion
   - Accessed: 2026-05-31

[10] **YouTube Hands-On Reviews**
    - Type: T3 — Video reviews
    - Accessed: 2026-05-31
    - Note: Referenced but specific video URLs not archived.

### UNSUPPORTED — Marked in Retrofit

[11] **Bloomberg: "Apple Vision Pro lite rumors"**
    - Originally cited URL: `https://www.bloomberg.com/news/articles/2026-05-15/apple-vision-pro-lite-glasses`
    - **Status: URL UNVERIFIED** — Bloomberg article slug not confirmed. Bloomberg paywall also limits access.

[12] **Ray-Ban AI SDK**
    - Originally cited URL: `https://developers.facebook.com/docs/ray-ban-ai`
    - **Status: URL UNVERIFIED** — Meta developer docs exist, but this specific path not confirmed.

## Confidence Reconciliation

| Original Claim | Original Grade | Revised Grade | Justification |
|---|---|---|---|
| Hardware specs (cameras, mics, compute) | [Verified] | [Directionally Correct] | iFixit URL unverified [1]; cross-reference with `meta-ray-ban-ai-glasses/` [7][8] |
| On-device LLM inference | [Verified] | **[CONTRADICTED]** | Meta Engineering blog [2] confirms AI is cloud-processed. `meta-ray-ban-ai-glasses/` report provides grounded T1 evidence contradicting this claim. **DOWNGRADED.** |
| 6–8 hours battery for AI use | [Verified] | [Directionally Correct] | Community reports [9]; contradicted by `meta-ray-ban-ai-glasses/` which cites ~4 hours from Tom's Guide [8] |
| Privacy controls (shutter + LED) | [Verified] | [Directionally Correct] | Meta public statements; specific privacy policy URL unverified [6] |
| "Fully AI-generated game by 2026" (Grok) | — | — | This claim belongs to Grok section, not this report |

### Key Contradiction Identified
The `ray-ban-ai-glasses/report.md` claims:
- "Llama-based vision-language model running **on-device**"
- "6–8 hours active AI use"

The `meta-ray-ban-ai-glasses/README.md` (with verified T1 sources) states:
- "**Almost nothing** runs on-device" — multimodal AI is cloud-processed [2]
- "~4 hours active use" from Tom's Guide [8]

**Verdict**: The `meta-ray-ban-ai-glasses/` version is better grounded with verified T1 sources. The `ray-ban-ai-glasses/` version (this report) contains claims that are **contradicted by the more thoroughly sourced report**.

## Reproducibility Note
Original research referenced teardown videos, FCC filings, and Meta blog posts, but several specific URLs were not verified. The `meta-ray-ban-ai-glasses/` report provides more grounded, verifiable source URLs.

```bash
# Verify Meta Engineering blog
web_extract --urls "https://engineering.fb.com/2025/03/04/virtual-reality/building-multimodal-ai-for-ray-ban-meta-glasses/"

# Check iFixit for real teardown URL
web_search --query "iFixit Ray-Ban Meta teardown 2025 2026"

# Check Wikipedia for baseline specs
web_extract --urls "https://en.wikipedia.org/wiki/Ray-Ban_Meta"

# X search for community reports
x_search --query "Ray-Ban Meta AI glasses 2026"
```
