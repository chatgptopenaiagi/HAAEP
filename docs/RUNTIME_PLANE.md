# Runtime Plane

Status: **CONCEPT / RESEARCH DIRECTION**. Genesis implements no runtime detectors, installers, or compatibility checks.

The Runtime Plane should describe the engineering environments relevant to a mission. Candidate adapters include .NET, Java/JVM, Node.js and npm, Python/Conda, Go, Rust/Cargo, C/C++, PHP, and accelerator runtimes. New adapters require a real task and evidence; the list is not a requirement to implement them all.

## Core distinction

**Present on the machine is not the same as required by the current mission.** Missing optional tools should not turn an unrelated mission into a broken environment. Installed tools should not automatically become dependencies.

| Question | Meaning |
|---|---|
| Present? | Evidence of an installation in the inspected scope |
| Active? | Which executable/environment the actual task resolves |
| Version and architecture? | Observed identity of the active and relevant alternative installations |
| Healthy? | Result of a named, bounded check; unknown without sufficient evidence |
| Required? | Relationship to an explicit mission or project requirement |
| Multiple installations? | Alternatives and possible conflicts, without assuming plurality is an error |
| Toolchain available? | Required compiler, SDK, build tool, package manager, or library capability |
| Environment active? | Task-specific context such as a virtual environment, Conda environment, container, or shell |

Health is scoped. A version command may prove that one executable starts; it cannot establish that an application builds, dependencies resolve, or a GPU workload works. Failure to inspect a protected or missing path is not proof of absence across the whole machine.

## Adapter responsibilities

Adapters should translate concrete tool evidence into the [engine contract](ENGINE_CONTRACT.md). They should retain source identity, collection time, scope, and gaps while avoiding raw environment dumps or secret-bearing configuration. Runtime-specific distinctions should remain available instead of being flattened into a misleading universal “installed” flag.

Observation must be bounded and explicit about side effects. Some tools can initialize state or contact services even when invoked for information. A future adapter must understand and disclose its probes rather than assuming every discovery command is passive.

## Pack composition

A technology pack can group coherent detectors, project requirement readers, build-tool adapters, AI tools, and a human playground. The Java example might include JVM/JDK inspection, compiler capability, and build-system interpretation. Pack presence must not grant installation or environment-mutation authority.

The human view should explain active versus alternative installations, task requirements, unsupported layouts, and uncertainty. A future reconciliation plan may propose the smallest required change, but inventory itself must not remove or normalize healthy installations for cleanliness.

## Evidence gate

Start with one mission, one runtime family, known sample environments, and failure/unknown fixtures. Verify active-path resolution in the relevant process context and test a bounded task capability before advertising support. Broader inventory and installation features remain separate blocks.

See [engine packs](ENGINE_PACKS.md), [OS plane](OS_PLANE.md), [GPU Compute Plane](GPU_COMPUTE.md), and [evidence law](EVIDENCE_LAW.md).
