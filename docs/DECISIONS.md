# Architectural decisions

This is an append-only decision log. Genesis decisions below were adopted on
**2026-09-26**. “Accepted” adopts an architectural constraint; it does not mean
the corresponding runtime is implemented. Supersede a decision through a new
record with a reason and evidence; preserve the old record.

## HAAEP-ADR-001 — Distinct Human and AI planes

**Status:** Accepted.

**Decision:** Keep the Human Plane and AI Plane distinct, connected through a
shared semantic core and engine contracts.

**Reason:** Humans need meaning, exploration, authorization, and final choice;
AI handles computation and engineering complexity. These are complementary
strengths, not a hierarchy of worth.

**Consequence:** Human and machine interfaces must consume the same authoritative
facts, permissions, action outcomes, and verification. A GUI must not become a
second engineering implementation. See [ARCHITECTURE](ARCHITECTURE.md).

## HAAEP-ADR-002 — Modular engines and explicit boundaries

**Status:** Accepted.

**Decision:** Grow through coherent engines, adapters, packs, providers, and
contracts. Add boundaries in response to evidenced requirements.

**Reason:** A long-lived platform needs independent testing and change without
becoming a monolith or a collection of speculative interfaces.

**Consequence:** Genesis defines contracts in prose and catalogs in READMEs; it
creates no empty engine implementations. A module name is not a support claim.
See [ENGINE_CONTRACT](ENGINE_CONTRACT.md) and [ENGINE_PACKS](ENGINE_PACKS.md).

## HAAEP-ADR-003 — Suitable engines expose human playgrounds

**Status:** Accepted.

**Decision:** Important, technically suitable engines should expose a meaningful,
safe human interface. Preserve Playground Law and its Chocolate Rule companion.

**Reason:** Hidden engineering complexity should return understandable,
explorable, controllable experiences to the person.

**Consequence:** A playground consumes engine contracts and exposes evidence,
experiments, comparison, and recovery limits. Decorative dashboards alone do not
satisfy the law. See [PLAYGROUND_LAW](PLAYGROUND_LAW.md).

## HAAEP-ADR-004 — Evidence precedes mutation

**Status:** Accepted.

**Decision:** Observe → evidence → understand → act → verify. Missing or
incomparable evidence remains unknown.

**Reason:** Confidence, exit codes, agent agreement, or the absence of an error
are insufficient proof of health or repair.

**Consequence:** Facts retain scope/provenance; proposals differ from grants and
outcomes; verification checks the intended objective. See [EVIDENCE_LAW](EVIDENCE_LAW.md).

## HAAEP-ADR-005 — Compare, return where possible, retain learning

**Status:** Accepted.

**Decision:** Come-and-Go learning requires state comparison and explicit
recoverability. Returning should retain useful evidence and lessons.

**Reason:** Learning is not exclusively forward execution; a worse experiment
can still teach. Not every action can be undone.

**Consequence:** Distinguish restoration, compensation, partial recovery,
unavailable recovery, and unknown recovery. A delta is not automatically a causal
explanation or evidence of improvement. See [STATE_DELTA_MODEL](STATE_DELTA_MODEL.md).

## HAAEP-ADR-006 — CWRE remains independent

**Status:** Accepted.

**Decision:** CWRE stays an external specialized compatibility/recovery system.
HAAEP may research an adapter contract; Genesis does not merge, rename, modify,
or import CWRE implementations.

**Reason:** Preserve healthy specialist state and continuity while avoiding
duplicated recovery logic and permission bypasses.

**Consequence:** Architectural lessons may inform HAAEP; actual integration
requires a later bounded mission and compatibility evidence. See
[CWRE_RELATIONSHIP](CWRE_RELATIONSHIP.md).

## HAAEP-ADR-007 — OS support requires real evidence

**Status:** Accepted.

**Decision:** Windows is the first evidenced direction from related CWRE work.
HAAEP has no implemented OS support at Genesis. WSL, Linux, macOS, and other
adapters require actual cases and tests.

**Reason:** Premature universal abstractions can hide material privilege,
filesystem, process, and security differences.

**Consequence:** Normalize only what is supported by evidence; preserve platform
specifics and unknowns. See [OS_PLANE](OS_PLANE.md).

## HAAEP-ADR-008 — Controlled adaptation

**Status:** Accepted.

**Decision:** Adaptation occurs through deliberate development, versioned
modules, reviewed rules, verified updates, and explicit permissions.

**Reason:** “Living” software must not imply silent self-modification or
unrestricted power.

**Consequence:** No silent self-rewriting, arbitrary downloaded execution,
automatic security weakening, or uncontrolled production mutation. Plugin and
pack presence never grants authority. See [SECURITY_MODEL](SECURITY_MODEL.md).

## HAAEP-ADR-009 — Private Genesis and pending licensing

**Status:** Accepted.

**Decision:** Create `chatgptopenaiagi/HAAEP` as a private repository. Licensing
remains pending; [LICENSE](../LICENSE) is a notice, not an open-source or
commercial license grant.

**Reason:** The mission explicitly defaults to private when public intent is
not established and forbids inventing a broad license preference.

**Consequence:** Do not infer distribution rights or publish private material.
An authorized owner may later review all content, dependencies, and licensing,
record a superseding decision, then use GitHub's repository visibility controls.
The installed GitHub CLI also documents `gh repo edit OWNER/REPO --visibility
public --accept-visibility-change-consequences`; recheck `gh repo edit --help`
and the consequences at the time of that decision. Recheck the resulting
visibility. This is a documented future procedure, not a Genesis action or grant.

## HAAEP-ADR-010 — Proposed semantics before platform implementation

**Status:** Accepted.

**Decision:** Genesis delivers prose contracts and explicitly labeled concepts.
It selects no implementation language, GUI framework, wire schema, or plugin
loader. Contract versioning is required in future implementations, but Genesis
does not declare a stable executable API.

**Reason:** Concrete examples and focused experiments should reveal which
abstractions work before they become compatibility commitments.

**Consequence:** Directory catalogs contain no fake implementations. Runtime
support and `VERIFIED` labels must name evidence and scope. A synthetic contract
experiment may validate semantics without proving live runtime support.

## HAAEP-ADR-011 — Shared action meaning and honest recoverability

**Status:** Accepted; amplified during Genesis.

**Decision:** Human and AI faces refer to the same scoped action proposal,
authorization, observed result, and verification. Changes to material scope or
preconditions require re-evaluation. Recovery semantics are part of the proposal.

**Reason:** Two presentation surfaces must not create two sources of truth.
CWRE's documented lesson about duplicated decision logic motivates conformance
checks; user control requires knowing what can actually be returned.

**Consequence:** A generated UI or agent cannot elevate a proposal into authority,
label an unverified action successful, or promise universal undo. Exact technical
binding and enforcement await an evidenced implementation. See
[ENGINE_CONTRACT](ENGINE_CONTRACT.md), [PLAYGROUND_CONTRACT](PLAYGROUND_CONTRACT.md),
and [SECURITY_MODEL](SECURITY_MODEL.md).
