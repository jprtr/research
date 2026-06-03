
# Home Assistant + Local LLM: Full Integration Stack

## Primary Sources

| Tier | Source | URL | Date |
|------|--------|-----|------|
| T1 | Home Assistant Official — Fully local voice assistant setup | https://www.home-assistant.io/voice_control/voice_remote_local_assistant/ | 2026-05 (living doc) |
| T1 | Home Assistant Ollama Integration Docs | https://www.home-assistant.io/integrations/ollama/ | 2024-04 (stable) |
| T1 | Wyoming Protocol Integration | https://www.home-assistant.io/integrations/wyoming/ | 2026-05 (living doc) |
| T2 | Joe Karlsson — GPU-accelerated local voice pipeline | https://www.joekarlsson.com/blog/local-voice-ai-home-assistant-gpu/ | 2026-04 |
| T2 | Stratobuilds — Ollama + Home Assistant performance matrix | https://stratobuilds.com/project/local-llm-ollama-home-assistant/ | 2025-2026 |
| T2 | TechTeamGB — HA Voice + Ollama Setup Guide | https://techteamgb.co.uk/2025/02/28/home-assistance-voice-ollama-setup-guide/ | 2025-02 |
| T2 | Local-LLM.net — Voice Assistant Pipeline | https://www.local-llm.net/guides/local-voice-assistant/ | 2026-04 |
| T2 | LocalScore AI Benchmarking | https://www.localscore.ai/blog | 2025-04 |
| T2 | Home Assistant Community — Local LLM Hardware Discussion | https://community.home-assistant.io/t/local-llm-hardware/835569 | 2025-01 |

## The Stack (All Open Source, All Local)

| Layer | Component | Function | Resource Intensity |
|-------|-----------|----------|-------------------|
| **Core Platform** | Home Assistant OS | Orchestration, device automation | Low |
| **LLM Engine** | Ollama | Runs local models (llama3.2, Qwen, gemma) | High |
| **Conversation Agent** | HA Assist / Ollama Integration | NLP intent parsing via LLM | Medium |
| **STT (Speech-to-Text)** | <div>
- Speech-to-Phrase (fast, limited)
- Whisper / faster-whisper (open, slow)
</div> | Converts voice to text | Low (S2P) to High (Whisper) |
| **TTS (Text-to-Speech)** | Piper | Neural voice synthesis | Medium |
| **Wake Word** | Wyoming / openWakeWord | Hotword detection | Low |
| **Hardware Interface** | USB Mic, speakers, ESP32 S3 Box | Audio I/O + voice satellite | Very Low |

## Key Technical Details

### Models That Work Well
- **Conversation:** llama3.2:3b (fastest), llama3.1:8b (better responses), Qwen 2.5 7B (good HA tool calling)
- **STT:** faster-whisper (GPU: <1s latency, CPU/Pi: ~8s), Speech-to-Phrase (<1s on Pi but limited grammar)
- **TTS:** Piper (1.6s voice per second on Pi, faster on x86)

### Hardware Sweet Spots

| Hardware | STT Latency | LLM Response | Power Draw | Cost |
|----------|-------------|--------------|-----------|------|
| Raspberry Pi 4/5 | 6–8s (Whisper) | Marginal on large models | 5–10W | Low |
| Intel NUC (i5/i7) | <1s | Good (3–9s per response) | 15–25W | Medium |
| SFF PC + RTX 3060 12GB | <1s | Excellent (<2s) | 54–180W | Medium |
| Mac Mini M4 Pro | <1s | Excellent | 25–50W | Higher |

### Wyoming Protocol: The Glue
Wyoming is Home Assistant's lightweight protocol for connecting voice services. It lets you run STT/TTS/wake-word on a separate machine from Home Assistant itself — e.g., a Pi for voice I/O, an NUC for the LLM engine. This is critical for performance tuning.

## So What?

1. **This is genuinely a differentiated smart home stack.** Alexa and Google Home are cloud-everything. A fully local voice assistant — wake word, STT, LLM reasoning, TTS — is achievable now and is a privacy/selling point that big tech cannot match without destroying their business model.

2. **Latency is the gate, not capability.** On a GPU-accelerated box, the pipeline is under 2 seconds end-to-end. On a Pi, it is 6–10 seconds. The gap is hardware, not software — so the question for a product play is "what hardware do you bundle?"

3. **Tool calling is the moat.** Home Assistant's Assist pipelines integrate with 1000+ devices. The LLM doesn't just chat — it turns lights on, adjusts thermostats, checks cameras. The moat is Home Assistant's integration ecosystem, not the LLM itself.

4. **Voice satellite hardware is a gap.** ESP32-based voice satellites are still marginal on quality. USB mics + Pi work but feel DIY. A polished, local-first smart speaker (think Sonos quality + Home Assistant brain) does not exist commercially.

5. **Viability for a a venture concept:** Moderate-to-good. The stack is open source and mature. A venture angle could be:
   - **Packaged local-first smart home hub** (NUC + HA + Ollama pre-configured, sold with a voice satellite)
   - **Privacy-first enterprise deployment** (legal/compliance offices that can't use Alexa)
   - **Offline cabin/rural** (no internet required — genuine differentiator)
   - **Content play:** "Build your own local AI assistant" guide/course

## Confidence & Caveats

| Claim | Confidence | Caveat |
|-------|------------|--------|
| Full local voice pipeline is deployable today | **High** | Verified by multiple community guides + official docs |
| Ollama runs LLM for HA conversation | **High** | Official integration, stable since 2024.4 |
| GPU significantly outperforms CPU | **High** | Benchmarked on LocalScore; faster-whisper is CUDA-optimized |
| RPi 5 can handle the stack | **Medium** | Works but slow. GPU box or Mac Mini recommended for real-world use |
| Piper is best-in-class local TTS | **Medium** | Kokoro is emerging as a competitor with better voice quality |

## Sources Freshness

- Official HA docs: **Live** (continuously updated, Wyoming is actively developed)
- Ollama integration: **2024** (stable for 1+ year, widely used)
- Community performance benchmarks: **2025-2026** (Joe Karlsson article most recent at Apr 2026)
- Hardware benchmarks: **2025-04** (LocalScore framework active)

---
