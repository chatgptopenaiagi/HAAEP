# Local AI direction

Status: **CONCEPT / RESEARCH DIRECTION**. HAAEP has no model discovery, inference integration, routing, or supported-model list.

Local AI may complement cloud agents and Codex. The architecture should support cloud **and** local execution where the mission, capabilities, privacy requirements, resources, and human choices justify it. Qwen is an initial example, not a permanent dependency or platform identity. Ollama and llama.cpp are possible provider infrastructures to investigate; neither is integrated by Genesis.

## Proposed provider boundary

`ILocalModelProvider` is a conceptual contract name, not a shipped interface or SDK. A future concrete contract should answer bounded questions:

| Area | Information or operation |
|---|---|
| Discovery | Available models, source, installation location, and provider identity |
| Metadata | Model identifier, revision, format, declared capabilities, and applicable license reference |
| Limits | Context and input/output constraints, with the source of each limit |
| Resources | RAM/VRAM estimates, active allocation, accelerator requirements, and uncertainty |
| Execution | Supported inference modes, task request, cancellation, and bounded resource use |
| Health | Provider reachability, model availability, tested capability, and failure evidence |
| Results | Output, usage, timing, completion status, and verification limitations |

A listed model is not necessarily loaded, compatible, healthy, or suitable for a task. Resource estimates are not a guarantee that a workload will fit. Declared capabilities require task-relevant verification.

## Routing and data boundary

Routing should use the mission's requirements and explicit data handling policy. It must explain why a provider was selected and preserve the ability to choose another supported route. A local failure must not silently send private prompts, files, or evidence to a cloud service.

Provider access, model downloads, executable installation, and inference are distinct actions with separate permissions and costs. Model or provider discovery must not automatically download or execute code. Model artifacts, provenance, licenses, and required trust decisions need review before a supported integration can be claimed.

Local execution is not a universal privacy guarantee. Providers may log requests, expose network endpoints, load extensions, or have their own telemetry. Future adapters must describe the actual observed boundary rather than equating “local” with “safe.”

## Dual face

The AI face may expose capabilities and bounded task requests. The human face should show the selected provider/model, applicable limits, resource pressure, expected data destination, live task status, comparison results, and cancellation. A simple experiment should allow a human to compare useful outcomes without hiding quality or resource tradeoffs.

## First research gate

Choose one real task and one provider in an isolated experiment. Establish supported versions and provenance, test the exact required capability, document data flow and cancellation behavior, and report failure/unknown states. Do not infer general Qwen or local-model support from one successful response.

See [GPU Compute Plane](GPU_COMPUTE.md), [engine contract](ENGINE_CONTRACT.md), [playground contract](PLAYGROUND_CONTRACT.md), and [security model](SECURITY_MODEL.md).
