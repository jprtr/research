# Research: NemoClaw + RTX Spark Stack

## Version History
- **Original publication**: 2026-06-02
- **Updated**: 2026-06-03
- **Changes**: Added version history; aligned with Vanguard Research Directive. Report already has inline confidence and a clear "What's Still Open" section. All source claims are NVIDIA-sourced (noted as limitation).

## Cross-Report Notes
- **`local-ai-hardware-landscape/`**: Detailed NVIDIA hardware analysis including RTX Spark specs. This report complements it with the enterprise software stack angle.
- **No contradictions found** with other reports in repository.

## Key Findings

| Finding | Source | Confidence |
|---------|--------|------------|
| NemoClaw officially supports RTX Spark laptops as a deployment target | nvidia.com/en-us/ai/nemoclaw/ | High |
| Single-command installer (`nemoclaw.sh`) bundles Node.js, OpenShell, NemoClaw CLI, sandbox wizard, policy tiers, network presets | build.nvidia.com/spark/nemoclaw | High |
| NemoClaw blueprint expanding across full NVIDIA local AI lineup: GeForce RTX, RTX PRO, RTX Spark, DGX Spark, DGX Station | blogs.nvidia.com/blog/rtx-ai-garage-computex-spark-local-agents/ | High |
| Enterprise software vendors building agents with NVIDIA stack: NemoClaw blueprints, Nemotron models, OpenShell runtime, CUDA-X | nvidianews.nvidia.com | High |
| Inference routed to local Ollama on Spark — not cloud | build.nvidia.com | High |

## The Stack Architecture

| Layer | Component | What It Does |
|-------|-----------|--------------|
| **Hardware** | RTX Spark (128GB unified memory, Blackwell, 1 petaflop FP4) | Local compute node |
| **Security Runtime** | OpenShell | Sandboxed execution, declarative permission policies |
| **Agent Framework** | NemoClaw (OpenClaw wrapper) | Enterprise guardrails, policy-based privacy, network presets |
| **Models** | Nemotron (local) | Proprietary NVIDIA models, runs local |
| **Inference** | Ollama | Local LLM serving |
| **Integration** | Agent Toolkit | Windows-native AI hooks, messaging channels (Telegram/Discord/Slack) |

## The Enterprise Angle

NVIDIA isn't selling RTX Spark as a consumer toy. They're selling it as an **enterprise agent node** that happens to fit on a desk. The bundling tells the story:

- **NemoClaw** = enterprise security wrapper (the thing CISOs need to say yes)
- **OpenShell** = runtime containment (the thing security teams need to monitor)
- **OCSF JSON audit exports** = SIEM ingest (the thing compliance needs)
- **Local inference** = data residency solved (the thing legal needs)
- **Single installer** = deployment friction removed (the thing IT needs)

This is the same playbook as the Mac Mini M4 Pro phenomenon — prove consumer demand, let enterprise IT discover they can solve shadow-AI with a vendor-certified box.

## What's Still Open

| Unknown | Why It Matters |
|---------|---------------|
| Enterprise pricing / volume licensing | Is there a B2B SKU with management tooling? |
| Fleet management capabilities | Can you deploy 100 Spark nodes with centralized policy? |
| Third-party benchmarks | All claims are NVIDIA-sourced so far |
| Actual enterprise adopters | Who's piloting this beyond press releases? |

## Signal Log

- **2026-06-02**: Initial pattern identified — NemoClaw + RTX Spark as enterprise agent node
- **Status**: Active tracking. Awaiting enterprise pricing, pilot announcements, fleet management signals.
