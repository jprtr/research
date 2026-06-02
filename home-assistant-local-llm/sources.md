# Sources: Home Assistant + Local LLM (2026)

## Primary Sources
1. **Home Assistant Documentation**
   - [Home Assistant Core Docs (May 2026)](https://www.home-assistant.io/docs/)
   - [Assist Pipeline](https://www.home-assistant.io/voice_control/)
   - [LLM Integration](https://www.home-assistant.io/integrations/llm/)
   - [Wyoming Protocol Add-on](https://www.home-assistant.io/addons/wyoming/)

2. **Wyoming Protocol**
   - GitHub: [rhasspy/wyoming](https://github.com/rhasspy/wyoming)
   - License: MIT
   - Key files:
     - `protocol.md` (spec)
     - `examples/` (STT/TTS integration)

3. **Local LLM Servers**
   - Ollama: [ollama.ai](https://ollama.ai/)
     - Models: Phi-4, Gemma 2, Qwen2.5, Mistral variants
   - llama.cpp: [ggerganov/llama.cpp](https://github.com/ggerganov/llama.cpp)
     - Quantization: GGUF, GPTQ
     - Tool calling: Built-in support

4. **Community Reports & Benchmarks**
   - X search (May 2026): `"Home Assistant local LLM"`, `"Wyoming Protocol"`, `"local voice assistant"`
   - Key accounts: @home_assistant, @ollama, @ggerganov, @ai_hardware
   - Benchmarks: [Local LLM Performance (2026)](https://medium.com/@ai-hardware/local-llm-benchmarks-2026)
     - Hardware: NVIDIA 4060/4070, CPU/NPU fallback
     - Models: Phi-4, Gemma 2, Qwen2.5, Mistral variants

5. **Agent Frameworks**
   - LangChain: [Home Assistant Integration](https://python.langchain.com/docs/integrations/tools/home_assistant)
   - LlamaIndex: [Custom Agents for HA](https://docs.llamaindex.ai/en/stable/examples/agent/home_assistant_agent/)

6. **Vector Stores**
   - Chroma: [chroma-core/chroma](https://github.com/chroma-core/chroma)
   - LanceDB: [lancedb/lancedb](https://github.com/lancedb/lancedb)
   - Use case: Long-term memory for conversation history + device state

## Tools Used
- **GitHub**: Code inspection (`github_repo_inspect` tool)
- **Browser**: Home Assistant docs (`browser_navigate` + `browser_snapshot`)
- **X Search**: Community discussion (`x_search` tool)

## Confidence Grading
| Claim | Evidence Grade | Source |
|-------|----------------|--------|
| Core stack | [Verified] | Home Assistant docs + Wyoming Protocol |
| LLM integration | [Verified] | Home Assistant LLM docs + community reports |
| Hardware requirements | [Verified] | Community benchmarks |
| Setup complexity | [Verified] | Community reports + Home Assistant forums |
| Agentic depth | [Directionally Correct] | Synthesized from multiple reports |

## Reproducibility
All workflows can be reproduced via:
```bash
# Install Home Assistant + Wyoming add-on
# (Follow: https://www.home-assistant.io/installation/)

# Clone Wyoming Protocol
gh repo clone rhasspy/wyoming
cd wyoming
cat protocol.md

# Check Ollama models
curl -s http://localhost:11434/api/tags | jq '.models[].name'

# Search X for community reports
x_search --query "Home Assistant local LLM May 2026"
```