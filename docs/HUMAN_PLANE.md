# Human Plane

Status: **CONCEPT**. Genesis contains the architectural specification, not a desktop application or playground framework.

> Build complexity for AI, but always return an understandable, explorable and controllable world to the human.

The Human Plane helps people express intent, inspect evidence, explore alternatives, authorize consequential work, and understand outcomes. It preserves final agency while allowing bounded delegation.

## Responsibilities

| Surface | Human purpose |
| --- | --- |
| Projects and missions | State goals, constraints, success criteria, and authorized scope. |
| Explanations and inspection | Understand facts, inferences, unknowns, sources, and limitations. |
| Playgrounds and simulations | Explore a bounded experiment and its assumptions. |
| State comparison and return | See differences, evaluate outcomes, and use declared recovery options. |
| Decision and authorization controls | Accept or decline a concrete proposal with visible consequences. |
| Logs and progress | Observe execution, verification, failures, and remaining work. |

The future desktop may organize these surfaces into Home, Projects, Missions, AI Engines, Agents, Dragon-Hydra, ARX Evidence, System Health, GPU/CUDA, Runtimes, Playgrounds, State/Delta, Recovery, Logs, and Settings. These labels are navigation ideas, not current features or a fixed GUI specification.

## Boundary with engines

Human surfaces consume [engine contracts](ENGINE_CONTRACT.md) and [playground contracts](PLAYGROUND_CONTRACT.md). They may format, filter, and explain authoritative outputs, but must not silently introduce different diagnosis, risk, permission, or verification semantics. The same action requested through a human control or an AI tool must encounter the same authoritative checks.

Before consequential action, show what is proposed, why it serves the objective, what evidence supports it, the scope of change, recovery limits, and remaining unknowns. Afterward, show actual outcomes and verification rather than repeating the proposal as if it succeeded.

Usable defaults, accessible presentation, and progressive detail should make complexity navigable without concealing material facts. A safe preview must be distinguishable from a live action. If a surface cannot express an action's consequences accurately, it should support inspection or handoff rather than offer a misleading control.

See the [Caesar Principle](CAESAR_PRINCIPLE.md), [Playground Law](PLAYGROUND_LAW.md), and [security model](SECURITY_MODEL.md).
