# Sources: Home Assistant + Local LLM (2026)

## Version History
- **Original publication**: 2026-05-31
- **Updated**: 2026-06-03
- **Changes**: Numbered sources with tiering and staleness notes; marked unverified URLs; added access dates; reconciled confidence.

## Numbered Sources

### T1 — Primary / Authoritative

[1] **Home Assistant Documentation**
   - URL: https://www.home-assistant.io/docs/
   - Type: T1 — Official documentation
   - Accessed: 2026-05-31
   - Note: Authoritative source for HA capabilities, Assist pipeline, LLM integration.

[2] **Home Assistant Voice Control / Assist Pipeline**
   - URL: https://www.home-assistant.io/voice_control/
   - Type: T1 — Official documentation
   - Accessed: 2026-05-31

[3] **Home Assistant LLM Integration**
   - URL: https://www.home-assistant.io/integrations/llm/
   - Type: T1 — Official documentation
   - Accessed: 2026-05-31

[4] **Wyoming Protocol — GitHub**
   - URL: https://github.com/rhasspy/wyoming
   - Type: T1 — Open-source project
   - Accessed: 2026-05-31
   - Note: MIT license. Protocol spec and STT/TTS examples available.

[5] **Ollama**
   - URL: https://ollama.ai/ / https://ollama.com/
   - Type: T1 — Vendor project page
   - Accessed: 2026-05-31
   - Note: Supported models list, local serving docs.

[6] **llama.cpp — GitHub**
   - URL: https://github.com/ggerganov/llama.cpp
   - Type: T1 — Open-source project
   - Accessed: 2026-05-31
   - Note: GGUF quantization, tool calling support documented.

### T2 — High-Quality Secondary

[7] **LangChain — Home Assistant Integration**
   - URL: https://python.langchain.com/docs/integrations/tools/home_assistant
   - Type: T2 — Framework documentation
   - Accessed: 2026-05-31
   - Note: Specific URL needs verification — LangChain docs structure changes frequently.

[8] **LlamaIndex — Home Assistant Agent**
   - URL: https://docs.llamaindex.ai/en/stable/examples/agent/home_assistant_agent/
   - Type: T2 — Framework documentation
   - Accessed: 2026-05-31
   - Note: Specific URL needs verification.

[9] **Chroma — GitHub**
   - URL: https://github.com/chroma-core/chroma
   - Type: T1 — Open-source project
   - Accessed: 2026-05-31

[10] **LanceDB — GitHub**
   - URL: https://github.com/lancedb/lancedb
   - Type: T1 — Open-source project
   - Accessed: 2026-05-31

### T3 — Community / Informal

[11] **X (Twitter) Community Discussion**
   - Search terms: `"Home Assistant local LLM"`, `"Wyoming Protocol"`, `"local voice assistant"`
   - Type: T3 — Community discussion
   - Accessed: 2026-05-31
   - Key accounts: @home_assistant, @ollama, @ggerganov

[12] **Medium: "Local LLM Benchmarks 2026"**
   - URL: `medium.com/@ai-hardware/local-llm-benchmarks-2026`
   - **Status: UNVERIFIED** — Medium article not confirmed as a real, accessible page. Hardware performance claims (NVIDIA 4060/4070 benchmarks) in original report may have relied on this.

## Confidence Reconciliation

| Original Claim | Original Grade | Revised Grade | Justification |
|---|---|---|---|
| Core HA + Wyoming + LLM stack | [Verified] | [Verified] | T1 docs [1][2][3][4] are authoritative |
| LLM integration options | [Verified] | [Verified] | HA official docs [3] + framework docs [7][8] |
| Popular local models (Phi-4, Gemma 2, etc.) | [Verified] | [Verified] | Ollama [5] and llama.cpp [6] model lists confirm |
| Hardware requirements (4060/4070 sufficient) | [Verified] | [Directionally Correct] | Community reports [11]; specific benchmark source [12] unverified |
| Setup complexity reduced by community templates | [Verified] | [Directionally Correct] | Community observation [11]; no specific template audit |
| Agentic depth (reason over device states) | [Directionally Correct] | [Directionally Correct] | Synthesis of framework capabilities [3][7][8] |

## Reproducibility Note
Research was conducted using browser navigation of Home Assistant docs, GitHub repo inspection, and X search. **Manual** research cycle on May 31, 2026.

```bash
# Check Home Assistant docs
web_extract --urls "https://www.home-assistant.io/voice_control/" "https://www.home-assistant.io/integrations/llm/"

# Inspect Wyoming Protocol
gh repo clone rhasspy/wyoming
cd wyoming && cat protocol.md

# Check Ollama model availability
ollama list
# or: curl -s http://localhost:11434/api/tags | jq '.models[].name'

# X search for community reports
x_search --query "Home Assistant local LLM 2026"
```
