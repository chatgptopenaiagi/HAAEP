# Engine packs

Status: **CONCEPT**. Genesis defines composition boundaries. No pack installer, discovery service, marketplace, signing pipeline, or runtime loader exists.

A pack groups coherent technology-specific engines, adapters, providers, documentation, and human playgrounds. Different installations may select different packs while sharing common contracts. A pack is a distribution and composition unit; it must not become a second platform core.

## Example: Java pack

A future Java pack could group runtime discovery, JVM and JDK inspection, compiler and build-system adapters, project requirement inspection, machine-facing tools, and a human playground that compares installed toolchains with project needs. This is a proposed grouping, not a claim that these modules exist.

Windows, Linux, CUDA, CAD, Visual Studio, Go, Rust, Python, Qwen, ARX, Dragon-Hydra, and CWRE are further possible pack families. Each requires a real use case and evidence before implementation. A CWRE pack would integrate the independent project through a contract; it would not imply ownership or migration of CWRE into HAAEP.

## Proposed manifest responsibilities

An eventual manifest should declare pack identity and version, publisher or source provenance, compatible contract versions, included modules, required and optional dependencies, supported environments with evidence references, requested permissions, data-transfer behavior, human surfaces, and known limitations.

Dependency declarations must distinguish installation prerequisites from capabilities needed only for a particular mission. Installing a pack should not automatically install every possible external runtime or activate every available agent.

A manifest may request authority; it cannot grant it. Permissions belong to scoped grants evaluated at execution. A dependency does not inherit its caller's unlimited authority, and adding a new dependency cannot silently broaden an existing grant.

## Lifecycle expectations

Future pack admission should check provenance, compatibility, declared capabilities, and requested permissions before activation. A trusted signature could establish publisher identity and artifact integrity; it would not prove that the pack's actions are safe or correct.

Updates require a visible change summary, contract compatibility checks, tests, and a recovery strategy appropriate to changed state. Removal should preserve user projects, mission history, and independently owned runtimes by default. Pack removal and external package removal are separate operations.

Optional or incompatible modules should produce explicit unavailable or unknown capabilities rather than make the installation appear universally healthy. A failed pack must not silently invalidate unrelated healthy components.

## Questions deferred until evidence exists

Process isolation, package format, dependency resolution, signature infrastructure, permission delegation, and update distribution are future decisions. Genesis adopts no arbitrary script execution mechanism or trust-by-default plugin architecture.

Related: [architecture](ARCHITECTURE.md), [engine contract](ENGINE_CONTRACT.md), [security model](SECURITY_MODEL.md), and the [pack workspace](../packs/README.md).
