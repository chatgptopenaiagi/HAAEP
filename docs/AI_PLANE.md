# AI Plane

Status: **CONCEPT**. Genesis implements no agents, tool execution service, orchestration runtime, or inference provider.

The AI Plane performs engineering complexity in service of human intent. Potential responsibilities include coding, analysis, search, simulation, testing, verification, environment inspection, dependency reconciliation, runtime management, evidence processing, and bounded agent orchestration. Cloud AI, local models, and GPU execution are future execution options, not assumptions about available capability.

## Operating obligations

- Consume explicit mission objectives, constraints, success criteria, and authority.
- Obtain facts through documented engines and adapters, preserving provenance and uncertainty.
- Explain proposed actions through the same contracts consumed by the Human Plane.
- Execute only within granted scope and recheck relevant preconditions.
- Expose progress, meaningful events, verification results, failures, and recovery limitations.
- Preserve healthy state and continuity; do not treat a failed attempt as permission for broader mutation.
- Keep secrets out of ordinary logs, reports, and evidence exports.

The AI Plane can propose and execute authorized work, but cannot grant itself authority. A model-generated command, an agent's recommendation, or agreement among several agents is not sufficient evidence of safety or success.

## Shared core boundary

The [shared architecture](ARCHITECTURE.md) supplies proposed contracts for facts, evidence, state, permissions, events, and missions. Engines own coherent engineering logic. The Human Plane and AI Plane consume those same semantics; neither maintains a competing repair or verification implementation.

For a future runtime-selection mission, an AI tool might collect task requirements, compare candidate environments, and propose one bounded selection. The human sees the same evidence and consequences through a playground. Execution depends on the actual action's permission class, and verification checks the task outcome rather than merely trusting the tool's exit code.

## Future collaborators

[Dragon-Hydra](DRAGON_HYDRA_RELATIONSHIP.md) is a possible orchestration subsystem, [ARX](ARX_RELATIONSHIP.md) a possible evidence and reconciliation subsystem, and [CWRE](CWRE_RELATIONSHIP.md) an independent compatibility and recovery system. [Local-model providers](LOCAL_AI.md) and the [GPU Compute Plane](GPU_COMPUTE.md) may add execution capabilities. Genesis defines boundaries; it does not establish integrations or support claims.

See the [Evidence Law](EVIDENCE_LAW.md), [engine contract](ENGINE_CONTRACT.md), and [security model](SECURITY_MODEL.md).
