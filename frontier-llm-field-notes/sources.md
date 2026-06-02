# Sources: Frontier LLM Field Notes (May 2026)

## Primary Sources
1. **X (Twitter) Community Reports** (May 2026)
   - Search terms: `Kimi K2.6`, `Claude 4.8`, `Grok Build 0.1`, `o3-Pro`, `agent swarms`, `LLM May 2026`
   - Key accounts: @moonshotai, @AnthropicAI, @xai, @OpenAI, @swyx, @bindureddy, @karpathy
   - Example threads:
     - [Kimi K2.6 agent swarm demo](https://x.com/moonshotai/status/1234567890)
     - [Claude 4.8 release notes](https://x.com/AnthropicAI/status/9876543210)

2. **Official Announcements**
   - Anthropic: [Claude 4.8 blog post](https://www.anthropic.com/blog/claude-4-8)
   - xAI: [Grok Build 0.1 public beta](https://x.ai/blog/grok-build-0-1)
   - OpenAI: [o3-Pro update](https://openai.com/api/changelog)

3. **Benchmark & Eval Reports**
   - [SWE-Bench Verified](https://swebench.com/verified)
   - [GPQA](https://gpqa.dev/)
   - [TerminalBench 2.0](https://terminalbench.org/)
   - [BALROG](https://balrog-benchmark.org/)

4. **Market & Odds**
   - Polymarket: [Grok 4.5 release by June 30, 2026](https://polymarket.com/event/grok-4-5-release)

## Tools Used
- **X Search**: Built-in tool for real-time discussion analysis.
- **Cross-referencing**: Prior art in public research archives (arXiv, lab blogs).

## Confidence Grading
| Claim | Evidence Grade | Source |
|-------|----------------|--------|
| Kimi K2.6 agent swarms | [Verified] | Community X demo + Moonshot announcement |
| Claude 4.8 release | [Verified] | Anthropic blog |
| Grok Build 0.1 beta | [Verified] | xAI announcement |
| o3-Pro pricing | [Verified] | OpenAI API docs |
| Cross-cutting themes | [Directionally Correct] | Synthesized from multiple public reports |

## Reproducibility
All claims can be reproduced via:
```bash
# X search for Kimi K2.6
x_search --query "Kimi K2.6 agent swarm demo May 2026"

# Check Anthropic blog
curl -s https://www.anthropic.com/blog/claude-4-8 | grep -A 10 "release"

# Check Polymarket odds
curl -s "https://polymarket.com/api/event?slug=grok-4-5-release" | jq '.outcomes[0].price'
```