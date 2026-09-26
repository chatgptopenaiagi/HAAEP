# Adapters

Status: **CONCEPT catalog boundary; no adapter implementations**.

Adapters translate a specific operating system, runtime, tool, provider, or
external subsystem into an engine's contract. Preserve source provenance,
capability differences, unknown values, and errors. Do not flatten missing
evidence into a healthy result or implement a second permission policy.

Candidate directions include [OS adapters](../docs/OS_PLANE.md),
[runtime adapters](../docs/RUNTIME_PLANE.md),
[local-model providers](../docs/LOCAL_AI.md), and
[CWRE integration](../docs/CWRE_RELATIONSHIP.md). None is implemented.

Each future adapter needs a concrete source boundary, evidence-backed mapping,
supported/tested environments, permissions, redaction behavior, fixtures, and
failure/unknown tests. Do not force a universal OS abstraction before a second
environment supplies real evidence. See the
[engine contract](../docs/ENGINE_CONTRACT.md).
