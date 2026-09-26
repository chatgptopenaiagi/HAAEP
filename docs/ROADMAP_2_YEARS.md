# Two-year conceptual roadmap

Status: **DIRECTION, NOT DELIVERY PROMISE**. The horizon starts with Genesis in September 2026 and may extend beyond two years. Order and scope change only through explicit decisions supported by real problems and evidence.

The roadmap is a set of possible branches. It is not authorization to implement them simultaneously, a weekly schedule, or a commitment that every named integration will exist.

## Foundation / Year 0

Genesis establishes the mission, principles, architecture, proposed contracts, permission boundaries, engine/pack/playground concepts, state/delta direction, CWRE lessons, repository discipline, and durable progress/decision records.

The immediate next action is recorded only in [PROGRESS.md](PROGRESS.md). Future sessions must follow that bounded action rather than selecting a large roadmap item by enthusiasm alone.

Foundation is credible when the documents agree, current capability claims are accurate, the GitHub foundation is verified, and a future session can identify one precise next block. A diagram or contract proposal is not an implementation.

## Year 1: prove a small vertical path

| Direction | Evidence gate |
|---|---|
| Shared core and engine contract | A small real engine demonstrates facts, unknowns, permissions, results, and verification without duplicated GUI logic |
| Runtime inventory and Windows/Codex adapters | One scoped mission, repeatable fixtures, and observed environment behavior establish a support boundary |
| Basic playground framework | A human can inspect and understand an engine result, try a safe experiment, and compare outcomes |
| Mission framework | Intent, constraints, authorized actions, acceptance criteria, and stop conditions survive the full workflow |
| State snapshots | Sanitized comparable state can be captured and retained with provenance and explicit gaps |
| CWRE integration research | An external read-only contract can be consumed without copying rules or expanding repair authority |
| ARX integration research | Actual ARX capabilities and ownership boundaries are inspected before choosing an exchange contract |
| GPU foundation and local-model provider contract | One justified use case proves a bounded capability and transparent resource/data handling |

The intended result is a modest, testable path from human intent through an engine to an understandable human surface. “Shared core” does not mean building every general-purpose subsystem first.

## Year 2: expand only proven boundaries

| Direction | Evidence gate |
|---|---|
| Dragon-Hydra orchestration | Small bounded delegation, conflict handling, cancellation, and independent acceptance checks work reliably |
| Richer local AI and runtime packs | Distinct tasks justify additional providers/adapters and verified composition |
| WSL/Linux expansion | Real guest/native environments expose differences that shape tested common contracts |
| CAD experimentation and Visual Studio integration | A concrete engineering workflow justifies a narrow adapter and useful playground |
| Pack/plugin architecture | Stable capabilities and permission boundaries justify an installation and compatibility design |
| State/delta intelligence and recovery integration | Comparisons are valid, action plans are scoped, and restoration limits are demonstrated |
| Signed releases and distribution | A real executable artifact, supported environment matrix, release ownership, and verified update/rollback process exist |
| Desktop GUI and playground generation experiments | Engine contracts are mature enough for meaningful controls and transparent authority |

macOS and other environments remain possible later branches; no artificial date or parity promise is assigned to them.

## Gates for every development block

1. Discover a real problem and identify the human decision or experience it affects.
2. Model the smallest contract change that can express it, including unknown and failure states.
3. Implement one bounded capability, with authority no broader than required.
4. Test using synthetic or isolated cases before any authorized live operation.
5. Verify the stated outcome and record what remains unverified.
6. Document the result, preserve continuity, and leave one exact next action.

Progress should be judged by useful decisions, correctly diagnosed problems, false claims avoided, verified outcomes, understandable experiments, and preserved human agency. Feature counts and agent counts are not success metrics.

See [mission](MISSION.md), [principles](PRINCIPLES.md), [architecture](ARCHITECTURE.md), and [decisions](DECISIONS.md).
