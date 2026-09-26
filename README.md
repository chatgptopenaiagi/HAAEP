# HAAEP

**Human-AI Adaptive Engineering Platform** is the working name for a long-term,
modular engineering environment that connects human intent with AI engineering
capability. Its name may evolve; its central product law remains:

> Build complexity for AI, but always return an understandable, explorable and controllable world to the human.

**Current status: Genesis documentation foundation.** This repository defines
principles, architectural boundaries, and proposed contracts. It contains no
executable platform, working engines, desktop application, or installed packs.

## Two planes, one shared understanding

| Plane | Responsibility | Boundary |
| --- | --- | --- |
| [Human Plane](docs/HUMAN_PLANE.md) | Purpose, explanations, playgrounds, experiments, comparison, authorization, and final choice | Uses engine contracts; does not secretly duplicate engineering logic |
| [AI Plane](docs/AI_PLANE.md) | Analysis, coding, search, simulation, orchestration, tool execution, and verification | Makes actions and evidence visible; operates within explicit authority |

A proposed [shared core](docs/ARCHITECTURE.md) connects both planes through facts,
evidence, state references, permissions, events, and mission contracts. No runtime
or GUI technology has been chosen.

## Five major principles

1. **[Caesar Principle](docs/CAESAR_PRINCIPLE.md):** give computation to the machine;
   preserve human meaning, agency, responsibility, and final choice.
2. **[Playground Law](docs/PLAYGROUND_LAW.md):** important, suitable engines should
   provide safe ways to observe, understand, experiment, compare, return, and try
   again. The companion **Chocolate Rule** asks for a simple, useful, enjoyable
   human experience when technically reasonable.
3. **[Engine Law](docs/PRINCIPLES.md):** grow through coherent engines, adapters,
   packs, and contracts, with a GUI-independent engineering core.
4. **[Come-and-Go Law](docs/COME_AND_GO_LEARNING.md):** compare states, return when
   useful, and preserve what the experiment taught. Return is not failure.
5. **[Evidence Law](docs/EVIDENCE_LAW.md):** observe, gather evidence, understand,
   act, then verify. Unknown remains a valid state.

## Engines and playgrounds

An [engine](docs/ENGINE_CONTRACT.md) owns one coherent engineering capability.
Its AI face exposes facts, capabilities, plans, and results. Its human face
provides explanations and controls through a [playground contract](docs/PLAYGROUND_CONTRACT.md).
Both faces share the same underlying semantics and permission checks.

An [engine pack](docs/ENGINE_PACKS.md) could group a technology's detectors,
adapters, tools, and playgrounds. A Java pack, for example, might connect JVM/JDK
inspection with build tools and a human environment explorer. Pack discovery,
installation, trust, and distribution are concepts, not implemented services.

Playgrounds must support meaningful inspection and safe experimentation, not
merely decorate automation. [Metadata-generated playgrounds](docs/PLAYGROUND_GENERATOR.md)
are a research direction; metadata will not grant action authority.

## Independent systems and future directions

| System or direction | Proposed relationship | Genesis status |
| --- | --- | --- |
| [CWRE](docs/CWRE_RELATIONSHIP.md) | External compatibility, recovery, verification, and continuity specialist | Independent; untouched by Genesis |
| [ARX](docs/ARX_RELATIONSHIP.md) | Evidence and reconciliation subsystem behind a contract | Concept; no integration |
| [Dragon-Hydra](docs/DRAGON_HYDRA_RELATIONSHIP.md) | Bounded multi-agent orchestration | Concept; no swarm or integration |
| [Local AI](docs/LOCAL_AI.md) | Provider contracts for cloud + local collaboration; Qwen is one example | Research direction |
| [GPU Compute](docs/GPU_COMPUTE.md) | Capability inspection and governed workloads with human playgrounds | Research direction |
| [Runtimes](docs/RUNTIME_PLANE.md) and [operating systems](docs/OS_PLANE.md) | Evidence-based adapters; installed does not mean required | No runtime or OS support implemented |

## Two-year direction

The [roadmap](docs/ROADMAP_2_YEARS.md) is evidence-gated, not a release promise:

- **Foundation / Year 0:** principles, proposed contracts, safety boundaries,
  repository discipline, and small experiments that test architectural assumptions.
- **Year 1:** explore a minimal shared core, observed runtime and Codex/Windows
  adapters, specialist integration boundaries, provider/GPU foundations, basic
  playgrounds, missions, and snapshots.
- **Year 2:** consider bounded orchestration, richer packs and local AI,
  WSL/Linux evidence, CAD and Visual Studio experiments, state/delta and recovery,
  signed releases, a desktop surface, and playground generation research.

## What exists and what does not

**Exists:** the mission, adopted principles, proposed semantic contracts,
integration boundaries, decision log, progress record, mission template, and Git
foundation. Directory READMEs describe future module boundaries.

**Does not exist:** executable engines, OS or runtime adapters, CUDA/cuDNN or
Qwen integration, ARX/Dragon-Hydra integration, GUI, plugin installation,
marketplace, installer, self-update, or cross-platform orchestration. There are
no application tests or builds yet; Genesis validates documentation structure,
links, scope, Git state, and publication.

## Start or resume development

Read [AGENTS.md](AGENTS.md), [MISSION](docs/MISSION.md), [PROGRESS](docs/PROGRESS.md),
and relevant [decisions](docs/DECISIONS.md). Confirm the workspace and Git state,
then read affected contracts and run focused tests when code exists.

Follow the single `NEXT_EXACT_ACTION` in progress. Complete one coherent block:
discover → model → implement → test → verify → document → preserve → next exact
action. Keep progress current, commit the result, push when authorized, and stop.
Do not restart the architecture or attempt the whole roadmap each session.

Use the [mission template](missions/MISSION_TEMPLATE.md) to make scope, authority,
evidence, validation, and the stopping condition explicit.

## Repository policy

Genesis starts **private**. Licensing is **pending**; [LICENSE](LICENSE) grants no
project-wide license. A later owner decision may change either policy; the
[decision log](docs/DECISIONS.md) records the boundary and visibility procedure.
Private visibility does not make secrets suitable repository content.
