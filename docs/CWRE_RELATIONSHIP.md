# CWRE relationship

Status: **RESEARCH DIRECTION**. No HAAEP adapter or executable integration exists.

CWRE (Codex Windows Recovery Engine, with a longer-term adaptive-runtime direction) remains an independent specialized project. Its concerns are compatibility, diagnosis, recovery, adaptation, repair, verification, and continuity. HAAEP must not rename, absorb, relocate, or silently modify CWRE.

## Division of responsibility

| Responsibility | Owner in the proposed relationship |
|---|---|
| Observe and diagnose a supported CWRE environment | CWRE |
| Define CWRE rules, repair eligibility, and repair verification | CWRE |
| Explain a returned result within a larger mission | HAAEP Human Plane |
| Coordinate an explicitly authorized integration request | HAAEP adapter, subject to both systems' boundaries |
| Present repair choice and consequences | HAAEP Human Plane using CWRE's contract |
| Authorize consequential action | Human, under applicable policy |

HAAEP should consume a versioned contract rather than reproduce CWRE's diagnostic rules in its UI. A HAAEP permission grant must not bypass a CWRE precondition, approval requirement, or refusal. A CWRE result does not authorize unrelated HAAEP changes.

## Lessons observed during Genesis

Genesis read CWRE's local architecture documentation on 2026-09-26. This is a documentation review, not a new audit of its running software. No CWRE code, snapshots, configuration, or state were imported.

- Separate observation, rule evaluation, repair planning, and mutation.
- Preserve unknown evidence and distinguish unavailable observations from negative findings.
- Keep a workaround distinct from a repaired root cause.
- Attach verification to its actual scope: one verified operation does not prove whole-environment health.
- Preserve healthy state and back up important state before authorized mutation.
- Prefer capability and context evidence to broad assumptions based on version alone.
- Use shared contract examples to detect semantic drift. CWRE documents a case where two implementations of an execution-mode decision disagreed about unknown evidence.
- Do not mistake equal bytes or a successful build for complete supply-chain provenance or a supported distribution.

These lessons influence HAAEP's [engine contract](ENGINE_CONTRACT.md), [evidence law](EVIDENCE_LAW.md), and [security model](SECURITY_MODEL.md). They do not make CWRE's current internal types HAAEP's universal schema.

## First integration research boundary

A future bounded study should identify a supported CWRE version and read-only report surface, map a small sanitized result into HAAEP's fact/evidence model, and show the same result in machine and human forms. Unknown fields and unsupported versions must remain explicit.

Mutation integration needs a separate evidenced development block: plan identity, scope, approvals, backups, verification, rollback limitations, cancellation, and preservation of the original CWRE result. No automatic repair authority follows from installing an adapter.

## Open questions

- Which stable report fields can be consumed without depending on CWRE internals?
- How should the two systems negotiate contract versions and unsupported capabilities?
- How can HAAEP retain useful evidence without exporting sensitive local diagnostic detail?
- How will HAAEP present a scoped CWRE outcome without overstating overall health?

See [architecture](ARCHITECTURE.md), [state and delta model](STATE_DELTA_MODEL.md), and [roadmap](ROADMAP_2_YEARS.md).
