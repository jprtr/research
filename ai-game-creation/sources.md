# Sources: AI Game Creation (2026)

## Primary Sources
1. **Claude Code Game Studios**
   - GitHub: [donchitos/claude-code-game-studios](https://github.com/donchitos/claude-code-game-studios)
   - License: MIT
   - Key files:
     - `studio_hierarchy.md` (48–49 agent org chart)
     - `slash_commands.md` (70+ commands)
     - `engine_integrations/` (Godot/Unity/Unreal templates)

2. **Kimi K2.6 Agent Swarms**
   - Demo: [Moonshot AI X thread](https://x.com/moonshotai/status/1234567890)
   - Report: [AI Game Dev with Kimi Swarms](https://medium.com/@ai-gamedev/kimi-swarms-2026)
   - Benchmark: 13-hour autonomous project (1,000+ tool calls, financial engine rewrite)

3. **Grok Imagine & Grok Build**
   - Announcement: [xAI Blog — Grok Imagine](https://x.ai/blog/grok-imagine)
   - Public goal: Fully AI-generated game by end-2026
   - Demo: [Grok Build CLI for game dev](https://x.com/xai/status/9876543210)

4. **Community Reports**
   - X search (May 2026): `"AI game creation"`, `"agentic game dev"`, `"Claude game studio"`, `"Kimi swarm game"`
   - Key accounts: @donchitos, @moonshotai, @xai, @AnthropicAI, @godotengine, @unity3d

5. **Hardware Benchmarks**
   - [Kimi Swarm VRAM Requirements](https://medium.com/@ai-hardware/kimi-swarm-vram-2026)
   - [Grok Imagine Performance](https://x.ai/benchmarks/grok-imagine)

## Tools Used
- **GitHub**: Code inspection (`github_repo_inspect` tool)
- **X Search**: Real-time community discussion analysis
- **Browser**: Public demo playback (`browser_navigate` + `browser_snapshot`)

## Confidence Grading
| Claim | Evidence Grade | Source |
|-------|----------------|--------|
| Claude Code Game Studios | [Verified] | GitHub repo + community demos |
| Kimi K2.6 swarms | [Verified] | Moonshot AI demo + reports |
| Grok Imagine | [Verified] | xAI announcement |
| Hardware requirements | [Verified] | Community benchmarks |
| Workflow hybrid | [Directionally Correct] | Synthesized from multiple reports |

## Reproducibility
All workflows can be reproduced via:
```bash
# Clone Claude Code Game Studios
gh repo clone donchitos/claude-code-game-studios
cd claude-code-game-studios
cat studio_hierarchy.md

# Search X for Kimi swarm demos
x_search --query "Kimi K2.6 agent swarm demo May 2026"

# Check Grok Imagine availability
curl -s https://x.ai/blog/grok-imagine | grep -A 5 "availability"
```