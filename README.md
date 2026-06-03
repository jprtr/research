# AI Research Notes

A collection of structured research on artificial intelligence hardware, models, tools, and market dynamics. Each folder contains a self-contained research note with sourced claims, confidence ratings, and practical implications.

## Version History
- **Created**: 2026-05-31
- **Retrofit update**: 2026-06-03 — All reports retrofitted to comply with Vanguard Research Directive (inline citations, tiered sources, evidence-derived confidence, known unknowns, evidence matrices, cross-report notes).

## Topics

| Folder | Topic | Date | Confidence | Status |
|--------|-------|------|------------|--------|
| [frontier-llm-field-notes](frontier-llm-field-notes/) | Frontier LLM Field Notes (May 2026) | 2026-05-31 (updated 2026-06-03) | Medium (65%) | ✅ Retrofit complete |
| [path-to-agi](path-to-agi/) | Path to AGI: Timeline, Benchmarks, and Trajectory | 2026-05-31 (updated 2026-06-03) | Medium (60%) | ✅ Retrofit complete |
| [local-ai-hardware-landscape](local-ai-hardware-landscape/) | Local AI Hardware & Compute Landscape | 2026-06-01 (updated 2026-06-03) | Medium-High | ✅ Aligned (already well-structured) |
| [home-assistant-local-llm](home-assistant-local-llm/) | Home Assistant + Local LLM Integration Stack | 2026-05-31 (updated 2026-06-03) | High (78%) | ✅ Retrofit complete |
| [ai-game-creation](ai-game-creation/) | AI Game Creation: Tools, Market, and Gaps | 2026-05-31 (updated 2026-06-03) | Medium (65%) | ✅ Retrofit complete |
| [ray-ban-ai-glasses](ray-ban-ai-glasses/) | Meta Ray-Ban AI Glasses Teardown | 2026-05-31 (updated 2026-06-03) | Medium (68%) | ⚠️ Superseded — see meta-ray-ban-ai-glasses |
| [meta-ray-ban-ai-glasses](meta-ray-ban-ai-glasses/) | Meta Ray-Ban AI Glasses: On-Device AI Reality Check | 2026-05-31 (updated 2026-06-03) | Medium-High | ✅ Authoritative (verified T1 sources) |
| [nemoclaw-rtx-spark](nemoclaw-rtx-spark/) | NemoClaw + RTX Spark Enterprise Stack | 2026-06-02 (updated 2026-06-03) | Medium | ✅ Aligned |

## Quality Notes from 2026-06-03 Retrofit

### Issues Identified and Fixed
1. **Fabricated URLs**: Placeholder X/Twitter status IDs (`1234567890`, `9876543210`) appeared in 4 reports. All marked as **UNVERIFIED/PLACEHOLDER**.
2. **Fabricated arXiv IDs**: `2605.12345` and `2605.67890` in `path-to-agi/` were suspiciously round numbers. Marked as **UNSUPPORTED**.
3. **Unverified Medium articles**: Several `medium.com/@*` URLs could not be confirmed as real pages. Claims resting solely on these sources were downgraded.
4. **Missing inline citations**: All report.md-format reports lacked `[N]` inline citations. Now added.
5. **Confidence was guessed**: All reports had round-number confidence (70%, 75%, 80%) without derivation. Now derived from evidence base.
6. **Contradiction resolved**: `ray-ban-ai-glasses/` claimed on-device LLM and 6–8 hour battery; `meta-ray-ban-ai-glasses/` (with verified T1 sources) demonstrated cloud-processed AI and ~4 hour battery. Resolved in favor of the grounded report.

### What Was Added
- Numbered, tiered sources (T1/T2/T3) with access dates and staleness notes
- Inline `[N]` citations throughout all report bodies
- Evidence matrices mapping claims → source tiers → confidence
- Derived confidence assessments with justification tables
- "Known Unknowns" sections listing unresolved gaps
- "Limitations & Gaps" sections (concrete, not boilerplate)
- "Cross-Report Notes" linking related entities across reports
- Version history metadata in every report

## Methodology (Directive Compliance)

All reports now follow the **Vanguard Research Directive**:
- **Source tiering**: T1 (official docs, APIs, papers) > T2 (quality blogs, news) > T3 (X/Twitter, forums, community)
- **Inline citations**: Every factual claim carries `[N]` references
- **Evidence matrices**: Key claims mapped to source tiers with confidence
- **Derived confidence**: Based on source count, quality, agreement, and recency — not guessed
- **Non-fabrication**: No invented facts, URLs, benchmarks, or attributions
- **Gap honesty**: Unknown/unverified information is explicitly stated as such
- **Reproducibility**: Search queries, tools, and manual processes documented

## License

Research content is provided as-is for informational purposes.
