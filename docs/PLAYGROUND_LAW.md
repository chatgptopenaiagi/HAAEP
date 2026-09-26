# Playground Law

Status: **ADOPTED principle**. All playground behavior described here is **CONCEPT** during Genesis.

Whenever an engine, subsystem, simulation, or complex component is sufficiently important and technically suitable, it should expose a safe human-accessible playground. Suitability depends on a real task and a useful interaction, not on whether a UI can be generated.

A playground enables the human to **OBSERVE → UNDERSTAND → EXPERIMENT → COMPARE → RETURN → MODIFY → TRY AGAIN**. This is a set of possible interactions, not a promise that every engine can support every step.

## Required qualities

- Present facts, provenance, freshness, and uncertainty in understandable language.
- Consume the authoritative engine contract instead of duplicating engineering logic.
- Clearly distinguish observation, simulation, a proposed action, and an applied action.
- Keep experiments scoped and favor synthetic data, isolated workspaces, or verified reversible operations.
- Compare outcomes against an explicit objective and show relevant losses as well as gains.
- State what can be returned to, what recovery requires, and what cannot be undone.
- Apply the same permission rules as the AI interface; a button is not an authorization bypass.

A playground may be a GUI, graph, dashboard, timeline, 3D viewer, terminal surface, or another interaction that serves the task. An explanation-only view can be appropriate when experimentation would be misleading or unsafe. Record why an important engine lacks a playground rather than adding decoration to satisfy a checklist.

## Chocolate Rule

When AI completes difficult hidden engineering work, it should, where technically reasonable, return a simple, useful, enjoyable way for the human to experience what was created. Enjoyment must not hide risk, uncertainty, cost, or loss of control.

For a future GPU engine, this might mean an understandable compatibility view and a bounded workload experiment. For a future CAD engine, it might mean inspecting and comparing generated geometry. These are examples of direction, not implemented capabilities.

The [playground contract](PLAYGROUND_CONTRACT.md) defines the proposed boundary. [Playground generation](PLAYGROUND_GENERATOR.md) explores how metadata might help without assuming that generated interfaces can safely represent every domain.
