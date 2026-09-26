# Playground contract

Status: **CONCEPT**. No HAAEP playground framework or desktop GUI is implemented. This contract describes what a future human surface must communicate and control.

A playground lets a person **observe, understand, experiment, compare, return, modify, and try again**. It may be a graph, form, terminal surface, timeline, simulation, 3D viewer, or simpler explanation and comparison view. Suitability matters more than visual complexity.

## Shared engineering meaning

The playground consumes the [engine contract](ENGINE_CONTRACT.md). It may format and explain results, but the engine remains the authority for engineering facts, capability evaluation, action plans, and verification. The UI must not recalculate a competing repair rule or make an agent's proposal appear authorized.

| Surface | Required meaning |
| --- | --- |
| Context | Mission objective, inspected scope, observation time, and whether data is synthetic, simulated, or live |
| State | Known facts, unknowns, limitations, and evidence references in understandable form |
| Explanation | What was found, why it matters, and what the evidence can and cannot establish |
| Experiment | Inputs, allowed ranges where meaningful, expected effects, resource limits, and simulation or live-action mode |
| Comparison | Baseline and candidate identity, comparable fields, changed values, and uncertainty |
| Action | Concrete plan, scope, risk, permissions, irreversible effects, and verification expectation |
| Return | Recovery availability, prerequisites, limitations, and the result of any attempted restoration |

## Controls and agency

Observation should be accessible without accidentally triggering an experiment or modification. Controls distinguish inspecting, previewing, simulating, proposing, authorizing, and executing. Labels must describe the real effect; a button called “Try” cannot conceal a live installation or paid inference request.

Consequential choices retain human authorization. The authoritative executor enforces permissions even if a control is hidden or disabled. An AI-generated explanation or UI does not supply a grant. When a plan changes after approval, the surface must present the changed plan and applicable approval requirement.

Experiments should favor temporary or isolated state and bounded resources. A simulation that calls external services, consumes substantial compute, or writes files must disclose and classify those effects; “simulation” is not a blanket promise of harmlessness.

## Comparison and return

Keep the selected baseline identifiable. A visual difference alone does not prove improvement, damage, or causality. Show whether comparison was complete, partial, or unavailable and evaluate improvement against the stated objective.

Return can mean restoring a supported state, applying a compensation, or selecting an earlier view. These are different operations and require different labels. A viewing history is not a system backup. Disable or explain unsupported restoration rather than presenting a universal Undo button.

Retain the experiment's evidence and lessons after a return, subject to retention and privacy rules. See [Come-and-Go learning](COME_AND_GO_LEARNING.md) and the [state/delta model](STATE_DELTA_MODEL.md).

## Accessibility and failure behavior

Use readable text, keyboard access, and non-color-only status indicators where the chosen surface supports them. Offer a concise explanation first with evidence available for inspection. Progress, cancellation limits, partial execution, failed verification, and recovery failure must be visible.

Unknown or unsupported metadata should yield an honest explanation or a limited inspection surface. It must not silently become a healthy status, a permitted action, or an executable script.

Future conformance examples should show a useful human experience for both success and uncertainty, including at least one comparison that cannot justify a conclusion. See [Playground Law](PLAYGROUND_LAW.md) and [generator research](PLAYGROUND_GENERATOR.md).
