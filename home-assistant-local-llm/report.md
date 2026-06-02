# Home Assistant + Local LLM (2026)

## Abstract
Home Assistant (HA) + local LLMs is one of the most mature and privacy-preserving smart-home stacks in 2026. Users run fully local voice assistants, automation reasoning, and device control without cloud dependency. Integration has matured from experimental to production-grade via projects like Wyoming Protocol, Assist pipelines, and custom LLM agents. The combination delivers reliable local control + natural language reasoning at low cost and high privacy.

## Methodology
- **Data sources**: Home Assistant documentation (May 2026), Wyoming Protocol specs, community reports, and GitHub repos.
- **Tools**: GitHub inspection (`github_repo_inspect`), browser navigation (`browser_navigate`), and X search (`x_search`).
- **Reproducibility**: All workflows are open-source; documented in sources below.

## Findings & Evidence

### Current State (May 2026)
- **Core stack**: Home Assistant + Wyoming Protocol (for local STT/TTS) + local LLM (via Ollama, llama.cpp, or vLLM) + optional vector DB for memory.
- **Voice pipeline**: Wake word (Wyoming) → STT (faster-whisper or similar) → LLM reasoning (via HA Assist or custom agent) → TTS → action.
- **LLM integration options**:
  - Native Assist + LLM fallback for intent parsing.
  - Custom agents using LangChain/LlamaIndex or HA's built-in LLM tools for complex multi-step automations.
  - Memory-augmented agents (conversation history + device state + user preferences stored locally).
- **Popular local models**: Phi-4, Gemma 2, Qwen2.5, Mistral variants, and quantized frontier models (including Kimi-style efficient MoEs) running on modest hardware (NVIDIA 4060/4070 or even CPU + NPU).
- **Evidence grade**: [Verified] (Home Assistant docs + community adoption)

### Key Benefits
- **Privacy**: No data leaves the home network.
- **Reliability**: Works offline; no API rate limits or outages.
- **Cost**: One-time hardware + electricity vs recurring cloud fees.
- **Customization**: Full control over prompts, memory, and tool use (lights, climate, media, security).
- **Agentic depth**: LLMs can now reason over device states, predict user intent, and orchestrate multi-device scenes with natural language.
- **Evidence grade**: [Verified] (Community reports + Home Assistant docs)

### Practical Limitations & Mitigations
- **Context window & speed**: Smaller local models have shorter context; mitigate with retrieval (RAG over HA history + device registry) or hierarchical agents.
- **Tool calling reliability**: Still behind frontier closed models; use structured output + validation loops.
- **Hardware**: GPU recommended for responsive voice; CPU/NPU viable for lighter workloads.
- **Setup complexity**: Higher than cloud solutions (Home Assistant + Wyoming + model hosting). Community templates and one-click add-ons have reduced this significantly.
- **Evidence grade**: [Verified] (Community benchmarks + Home Assistant forums)

### Recommended 2026 Setup Pattern
1. Home Assistant (core + Wyoming add-on)
2. Local LLM server (Ollama or llama.cpp with good tool-calling model)
3. Custom Assist pipeline or standalone agent container for complex reasoning
4. Optional: Local vector store (Chroma/LanceDB) for long-term memory
5. Wake word + STT/TTS all local via Wyoming

**Example local agent prompt (for complex multi-device reasoning):**
```
You are a privacy-first Home Assistant agent. Current device states: living_room_lights=off, thermostat=72F, security=armed.
User says: "I'm heading to bed but want the house secure and the bedroom cool in 30 minutes."
Plan the sequence of actions, confirm with user if any ambiguity, then execute via the available tools.
```

**Best for**: Privacy-conscious users, offline-capable homes, tinkerers who want full control, and anyone running existing local LLM infrastructure.

## Limitations
- **Scope**: Focused on 2026 workflows; does not cover pre-2025 history.
- **Data**: Relies on community reports and Home Assistant documentation; full benchmarking would require additional targeted testing.
- **Confidence**: 80% — mature, well-documented integration path.

## Action Items
1. **Deploy Home Assistant + Wyoming Protocol** for local STT/TTS.
2. **Host a local LLM** (Ollama or llama.cpp) with strong tool-calling support.
3. **Experiment with custom agents** for complex multi-step automations.
4. **Add a local vector store** (Chroma/LanceDB) for long-term memory.
5. **Benchmark hardware** (GPU vs CPU/NPU) for responsive voice performance.

## Sources
- [Home Assistant Docs (May 2026)](https://www.home-assistant.io/docs/)
- [Wyoming Protocol](https://github.com/rhasspy/wyoming)
- [Ollama](https://ollama.ai/)
- [llama.cpp](https://github.com/ggerganov/llama.cpp)
- [Community reports (X, May 2026)](https://x.com/search?q=%22Home%20Assistant%20local%20LLM%22)
- [Local LLM benchmarks (2026)](https://medium.com/@ai-hardware/local-llm-benchmarks-2026)