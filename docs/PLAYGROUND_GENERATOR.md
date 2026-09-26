# Playground generator research

Status: **RESEARCH DIRECTION / CONCEPT**. No dynamic GUI generator exists or is authorized for implementation during Genesis.

The hypothesis is that bounded engine metadata can supply useful default human surfaces, reducing repetitive UI work while preserving the engine's authoritative semantics. Complex spatial, engineering, or accessibility needs may still require carefully authored interfaces.

## Minimum proposed metadata

| Metadata | Why a surface needs it |
| --- | --- |
| Engine and contract identity | Reject incompatible interpretations and identify the source |
| Observable fields | Name, meaning, type, units, knowledge state, scope, and provenance |
| Capabilities | Requirements, availability, limits, and explanations |
| Inputs | Meaning, validation constraints, defaults with rationale, and sensitive-data handling |
| Outputs | Interpretable results, evidence references, and relevant comparison semantics |
| Action references | Engine-owned plan generation and execution boundaries, declared effects and required permissions |
| Experiment hooks | Whether synthetic, simulated, or live; resource and side-effect constraints |
| Comparison and recovery | Comparable fields, supported baseline references, and actual recovery limits |

Metadata should reference authoritative operations, not embed unrestricted executable code. A renderer must validate data and escape untrusted content. A declaration that an action is safe cannot override policy, scope, preconditions, or engine verification.

## Potential benefits

- Consistent explanations, permission presentation, unknown states, and comparison controls across packs.
- A basic inspection surface for new engines before a specialized playground exists.
- Reuse of accessible components and a smaller chance of duplicating engineering logic in each UI.
- Human and AI views grounded in the same versioned records.

## Risks and constraints

Generic forms can hide domain meaning, overwhelm users, or suggest misleading precision. Metadata can be incomplete, stale, malicious, or incompatible. A generated control can make a consequential action look trivial. Rich plots can imply causality that the evidence does not establish.

The renderer must disclose limitations, separate observation from action, preserve units and uncertainty, and avoid inventing defaults for unknown semantics. Unsupported action metadata should fail closed for execution while preserving safe read-only explanation where possible. Domain-specific views need explicit review; automatic generation is not proof of usability.

Generation must never grant permissions or bypass the [engine](ENGINE_CONTRACT.md) and [security](SECURITY_MODEL.md) contracts. Pack metadata and agent-generated content are untrusted inputs at this boundary.

## Future experiment boundary and open questions

A future bounded research experiment could render synthetic facts and a comparison without any live-action controls. It would test whether a person can identify the baseline, explain an unknown, and understand why a capability is unavailable. This is a research option, not a second scheduled next action; [progress](PROGRESS.md) owns sequencing.

Questions remain: which metadata semantics are sufficient, which domains need custom interaction, how compatibility evolves, how generated explanations remain faithful, and how usability and accessibility are assessed. Choose a GUI technology only after an actual experiment establishes its requirements.

Related: [playground contract](PLAYGROUND_CONTRACT.md) and [Human Plane](HUMAN_PLANE.md).
