# ARX relationship

Status: **CONCEPT / RESEARCH DIRECTION**. Genesis defines a boundary, not a working integration or a claim about ARX's existing implementation.

ARX is a proposed evidence and reconciliation subsystem in the HAAEP ecosystem. Its possible responsibilities include machine inspection, evidence capture, evidence graphs, requirement reconciliation, state reconciliation, verification, and environment comparison.

ARX must not automatically become the whole HAAEP core. HAAEP's Human Plane, mission intent, permission decisions, engine contracts, and pack boundaries remain independently defined.

## Proposed boundary

| Input to ARX | Possible output from ARX |
|---|---|
| Authorized observation scope and collection constraints | Sanitized observations with provenance and gaps |
| Requirements and referenced evidence | Satisfied, unsatisfied, conflicting, or unknown requirements |
| Comparable state references and mission objective | Explained differences and reconciliation proposals |
| A verification question and relevant observations | Scoped verification result with limitations |

Evidence should identify its producer, collection time, scope, interpretation limits, and applicable contract version. A derived conclusion must retain references to the observations that support it. An evidence graph is not an authority graph: recording a command, recommendation, or external instruction does not grant permission to execute it.

Reconciliation may propose a course of action. Execution belongs to an explicitly authorized engine workflow with its own preconditions and verification. ARX must not silently resolve disagreement by deleting inconvenient evidence or selecting the most confident agent's assertion.

## Human and AI faces

The AI face may support queries, requirement checks, comparison requests, and machine-readable reconciliation proposals. The Human Plane should expose the evidence chain, disagreements, missing observations, what changed, and why a proposed action follows.

A human should be able to inspect the sources of a conclusion, compare interpretations, and decline a proposal. Sensitive evidence may require a restricted local view rather than general export; omission must be visible without exposing the secret itself.

## Research gates

Before any integration claim, a future block must inspect the actual ARX project and available contracts. It must establish a small real use case, ownership boundaries, a versioned exchange format, permission checks, sanitized fixtures, and a verified round trip. A HAAEP-specific reimplementation of ARX is outside Genesis.

Open questions include evidence identity and retention, invalidation of stale conclusions, disagreement representation, trust in external collectors, and how independent verification differs from repeating the same inference.

See [evidence law](EVIDENCE_LAW.md), [engine contract](ENGINE_CONTRACT.md), [state and delta model](STATE_DELTA_MODEL.md), and [security model](SECURITY_MODEL.md).
