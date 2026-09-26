# HAAEP mission

Status: **ADOPTED PROJECT CHARTER**. Architectural capabilities described here are
**CONCEPT** unless implementation and scoped verification are recorded in
[PROGRESS](PROGRESS.md). Established at Genesis on 2026-09-26.

HAAEP is the working name for the **Human-AI Adaptive Engineering Platform**. It
is intended to evolve for approximately two years and potentially beyond. Naming
uncertainty must not block careful engineering.

> Build complexity for AI, but always return an understandable, explorable and controllable world to the human.

## Purpose

Connect human intent to AI engineering capability through a modular environment.
The human should receive meaning, visibility, experimentation, comparison,
understanding, choice, and final agency while AI handles engineering complexity.
The platform should progressively connect coding agents and the operating
systems, runtimes, tools, services, models, and engineering environments around
them. It is not a one-session application build.

## Permanent architectural direction

- A [Human Plane](HUMAN_PLANE.md) presents playgrounds, explanations, experiments,
  inspection, comparison, return, missions, and authorization. It consumes engine
  contracts instead of duplicating engineering logic.
- An [AI Plane](AI_PLANE.md) performs analysis, coding, search, simulation,
  automation, testing, orchestration, and verification within visible authority.
- A [shared core](ARCHITECTURE.md) relates interfaces, facts, state, evidence,
  events, permissions, and mission contracts. Engines own coherent capabilities;
  adapters translate boundaries; packs group related technology; providers remain
  replaceable. No particular application framework is mandated.
- The [five primary principles](PRINCIPLES.md) are Caesar, Playground, Engine,
  Come-and-Go, and Evidence. The Chocolate Rule accompanies Playground Law.
  Human strengths and machine strengths complement one another.
- A sufficiently complex [engine](ENGINE_CONTRACT.md) should offer both machine
  and human faces when suitable. A [playground](PLAYGROUND_CONTRACT.md) must make
  real capabilities understandable and controllable. Metadata-generated
  playgrounds are [research](PLAYGROUND_GENERATOR.md), not a Genesis feature.
- [State, delta, and reconciliation](STATE_DELTA_MODEL.md) should support
  experiment, comparison, return where possible, retained knowledge, and another
  attempt. Difference alone is not proof of cause or improvement.

## Independent specialists and future planes

[CWRE](CWRE_RELATIONSHIP.md) remains an independent compatibility, diagnosis,
recovery, adaptation, repair, verification, and continuity system. Genesis may
read lessons; it must not absorb, rename, or modify CWRE.

[ARX](ARX_RELATIONSHIP.md) is a prospective evidence/reconciliation specialist,
not automatically the shared core. [Dragon-Hydra](DRAGON_HYDRA_RELATIONSHIP.md)
is a prospective bounded orchestration subsystem, not authorization for an
uncontrolled agent swarm. Their integrations are conceptual.

[Local AI providers](LOCAL_AI.md) should allow cloud + local collaboration. Qwen
is an initial example, with Ollama, llama.cpp, or future providers as possible
infrastructure; HAAEP must not permanently bind to one model or vendor.

[GPU compute](GPU_COMPUTE.md), [runtimes](RUNTIME_PLANE.md), and
[operating systems](OS_PLANE.md) are future capability planes. Windows provides
the strongest related experience; HAAEP itself does not yet support any OS or
runtime through executable adapters. CUDA, cuDNN, PyTorch, TensorRT, ROCm,
DirectML, .NET, Java/JVM, Node/npm, Python/Conda, Go, Rust, C/C++, PHP, Git,
GitHub, containers, Visual Studio, CAD, databases, and web stacks may enter through
coherent engines/adapters/packs when real problems justify them. WSL, Linux,
macOS, and future OS support require actual evidence and tests.

A future desktop may expose projects, missions, AI engines, agents, evidence,
system health, GPU, runtimes, playgrounds, state/delta, recovery, logs, and
settings. This navigation is a product direction, not an implemented application.

## Authority, security, and adaptation

Human authority must cover consequential actions. Expose what is proposed, why,
supporting evidence, unknowns, expected changes, verification, and recoverability.
Distinguish observation, diagnosis, simulation, proposal, workspace modification,
environment modification, elevated modification, security-sensitive modification,
and destructive actions. See [SECURITY_MODEL](SECURITY_MODEL.md).

Packs, plugins, agents, and generated interfaces must not inherit unrestricted
power. “Living adaptive software” means controlled modular growth, evidence,
capability awareness, reviewed versioned modules, and verified updates. It does
not mean silent self-rewriting, arbitrary downloads, unauthorized production
changes, or autonomous security-policy weakening.

## Genesis deliverable and stopping condition

Create a private GitHub repository named HAAEP under the authenticated account,
with an appropriate observed local development workspace, Git origin, and main
branch. Establish the mission, principles, architecture, proposed contracts,
relationship boundaries, [two-year direction](ROADMAP_2_YEARS.md),
[decision log](DECISIONS.md), [progress](PROGRESS.md),
[session instructions](../AGENTS.md), and
[mission template](../missions/MISSION_TEMPLATE.md).

Licensing remains pending. No broad commercial or open-source grant is inferred.
Do not build the GUI, live runtime/GPU/local-model integration, OS adapters, CAD,
Dragon-Hydra swarm, ARX rewrite, plugin marketplace, installer, self-update, or
kernel driver during Genesis.

Genesis is complete after a coherent initial commit is pushed, the remote owner,
visibility, branch, commit, README rendering and documentation presence are
verified, the local working tree is clean, and progress contains exactly one
bounded next action. Stop then.

## Continuing development

Follow [AGENTS.md](../AGENTS.md) and the current `NEXT_EXACT_ACTION`. Use:

**DISCOVER → MODEL → IMPLEMENT → TEST → VERIFY → DOCUMENT → PRESERVE → NEXT EXACT ACTION**

Implement one coherent block, grounded in a real requirement. Preserve healthy
state and specialist boundaries. Record what exists, what is conceptual, what is
unknown, and what was verified. Do not redesign the entire system each session.
Roadmap entries are directions requiring evidence, not promises.
