# Sources

## Version History
- **Original**: 2026-05-31
- **Updated**: 2026-06-03 (T1 sources verified and annotated per Vanguard Research Directive)

## Tier 1 Sources (Primary Evidence)

### Hardware Teardown & Engineering Documentation

| Source | URL | Type | Why It Matters |
|--------|-----|------|----------------|
| iFixit teardown article | https://www.ifixit.com/News/113543/theres-groundbreaking-waveguide-tech-inside-metas-800-ar-glasses-but-dont-count-on-fixing-them | T1 — Teardown journalism | Real teardown coverage for Meta Display Glasses hardware; confirms waveguide, 600×600 HUD, 960mWh battery, zero repairability |
| Meta Engineering blog | https://engineering.fb.com/2025/03/04/virtual-reality/building-multimodal-ai-for-ray-ban-meta-glasses/ | T1 — Engineering disclosure | Official architecture source confirming multimodal AI is cloud-processed, not on-device |
| Qualcomm AR1 Gen 1 announcement | https://9to5google.com/2025/06/10/snapdragon-ar1-gen-1/ | T2 — Tech press | Snapdragon AR1 specification and NPU capability claims |
| Wikipedia — Ray-Ban Meta | https://en.wikipedia.org/wiki/Ray-Ban_Meta | T2 — Encyclopedic | Consolidated specs with sourcing trail |
| Tom's Guide review | https://www.tomsguide.com/reviews/ray-ban-meta-smart-glasses | T2 — Product review | Real-world battery life (~4 hours active), storage data |

**Note**: Qualcomm AR1 Gen 1 coverage is T2 because it is tech press reporting on a vendor announcement. The Qualcomm official product page was not directly verified.

### Regulatory Filings (Real FCC IDs)

| Source | URL | Why It Matters |
|--------|-----|----------------|
| FCC reporting via Android Authority | https://www.androidauthority.com/meta-smart-glasses-fcc-filing-3672710/ | Secondary reporting pointing to real FCC filings (model numbers G4QM, G4QR, G4QB, G4QS) |
| FCC reporting via Road to XR | https://www.roadtovr.com/meta-ray-ban-smart-glasses-2026-next-gen/ | Secondary source summarizing next-gen hardware direction from real FCC filings |

### Critical Corrections
- **FCC ID `2AHRD-RAYBAN2026`**: This identifier was fabricated. Real 2026 FCC model numbers are **G4QM, G4QR, G4QB, G4QS** variants.[cite:44]
- **On-device AI**: The glasses are **cloud-reliant**. The Meta Engineering blog confirms multimodal AI queries are sent to Meta's servers, not processed on-device.[cite:38]
- **Battery life**: ~4 hours active use per Tom's Guide review, not the 6–8 hours claimed in the companion `ray-ban-ai-glasses/` report.

## Key Hardware Specs (Verified)

| Component | Spec | Source |
|-----------|------|--------|
| SoC | Qualcomm Snapdragon AR1 Gen 1 | Wikipedia [T2] |
| Camera | 12MP ultra-wide (up from 5MP) | Wikipedia [T2] |
| Storage | 32GB (Gen 2) | Wikipedia [T2] |
| Battery | ~4 hours active use | Tom's Guide [T2] |
| Weight | ~49g (standard Wayfarer) | Wikipedia [T2] |
| Connectivity | Bluetooth 5.3, Wi-Fi | Wikipedia [T2] |
| Price | $299–$379 | Wikipedia [T2], Tom's Guide [T2] |

### Display Glasses (Separate Product, ~$800)

| Component | Spec | Source |
|-----------|------|--------|
| Display | 600×600 pixel HUD, right eye only | iFixit [T1] |
| Tech | Lumus geometric waveguide + micro-projector | iFixit [T1] |
| Battery | 960mWh | iFixit [T1] |
| Battery life | ~6 hours mixed use | iFixit [T1] |
| Repairability | Zero — glued shut | iFixit [T1] |

## Source Validation Notes

- **iFixit URL**: Opened and confirmed on 2026-06-03. Matches display glasses teardown content.
- **Meta Engineering URL**: Opened and confirmed on 2026-06-03. Confirms cloud-processed multimodal architecture.
- **9to5google AR1 URL**: Opened and confirmed on 2026-06-03.
- **FCC model numbers**: Traced via Android Authority reporting to real filings (G4QM variants).
- **No fabricated sources remain**: All placeholder X URLs and fabricated FCC IDs have been removed.

## Confidence Assessment

| Claim | Source Tier | Confidence | Notes |
|-------|-------------|------------|-------|
| Cloud-processed AI (not on-device) | T1 | **High (90%)** | Meta Engineering blog is definitive |
| Battery ~4 hours (non-display) | T2 | **Medium-High (75%)** | Tom's Guide review, real-world tested |
| Battery ~6 hours (display) | T1 | **High (85%)** | iFixit teardown |
| Hardware specs (SoC, camera, weight) | T2 | **Medium-High (75%)** | Wikipedia consolidated; not direct vendor spec page |
| Display glasses repairability | T1 | **High (95%)** | iFixit teardown with photos |
| FCC model numbers (G4QM etc.) | T2 | **Medium (65%)** | Tech press reporting on filings; direct FCC ID not verified |

## Reproducibility

```bash
# Verify teardown claims
web_extract --urls "https://www.ifixit.com/News/113543/theres-groundbreaking-waveguide-tech-inside-metas-800-ar-glasses-but-dont-count-on-fixing-them"

# Verify on-device vs cloud AI architecture
web_extract --urls "https://engineering.fb.com/2025/03/04/virtual-reality/building-multimodal-ai-for-ray-ban-meta-glasses/"

# Verify FCC model numbers via tech press
web_extract --urls "https://www.androidauthority.com/meta-smart-glasses-fcc-filing-3672710/"
web_extract --urls "https://www.roadtovr.com/meta-ray-ban-smart-glasses-2026-next-gen/"
```
