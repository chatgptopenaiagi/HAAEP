# Engine contract

Status: **CONCEPT**. This is a proposed semantic contract, not a released API, generated interface set, or executable schema. An implementation must publish its supported version and conformance evidence before being described as supported.

An engine owns one coherent class of engineering questions. Its core remains independent of a particular GUI, agent, command line, or transport. The machine and human interfaces describe the same facts, plans, and outcomes.

## Minimum semantic surface

| Record | Required meaning |
| --- | --- |
| Identity | Stable engine identity, module version, contract version, supported scopes, and known limitations |
| Observation | What was inspected, when, by which source or method, in which scope, and with what access limitations |
| Fact | A named value with units or type where relevant, explicit knowledge state, observation reference, and applicable context |
| Capability | A task-relevant ability and its evaluated requirements, with evidence for satisfied, unsatisfied, or unknown requirements |
| Explanation | Finding, supporting evidence, effect on the mission, uncertainty, and possible next step |
| Action plan | Target and bounded changes, prerequisites, risk, required permissions, expected effects, backup needs, verification, and recoverability |
| Outcome | Execution status, independently reported verification status, changed targets, evidence references, and recovery outcome when applicable |

Facts may be available even when action is unavailable. An engine may be observation-only. It need not invent repair or simulation functions to fill a uniform interface.

## Knowledge and evidence

For a fact, distinguish **KNOWN**, **UNKNOWN**, and **NOT_APPLICABLE**. A KNOWN fact carries an observed value; a known boolean value of false differs from an observation that could not be made. “Not installed” is a known absence only when the inspection method and scope support that conclusion. An inaccessible directory cannot prove package absence.

Preserve evidence source, capture time, scope, method, and relevant limitations. A process environment observation may not describe another user or a future process. Source freshness is judged against the question, not a universal timeout. Conflicting observations remain visible until reconciliation has evidence to resolve them.

Evidence is data, including when it contains natural language or agent output. Its content does not become instructions, permission, or executable code. Evidence export must be sanitized and should refer to sensitive local material by a restricted reference rather than copy it.

## Capabilities and requirements

A capability evaluation reports **AVAILABLE**, **UNAVAILABLE**, or **UNKNOWN** in a stated context. It identifies the decisive requirement rather than returning only a summary label. A known unmet mandatory requirement can make a capability unavailable while other requirements remain unknown; those unknowns are retained.

Presence, health, and mission requirement are separate facts. A runtime can be present yet unsuitable for a task; an absent runtime can be irrelevant to that task. Version information supports capability evaluation but does not replace evidence of behavior or compatibility.

## Plans and execution

A plan identifies the exact intended targets and effects at the precision necessary for safe authorization. It includes preconditions, expected resource use where consequential, external data transfers where relevant, cancellation limits, and whether the operation can be repeated safely. Uncertain effects must be visible before approval.

A plan is not an authorization. The executor checks the applicable grant against the proposed operation and rechecks relevant facts before mutation. A changed target, broader scope, or materially changed plan invalidates approval for the old plan. Agents and human controls both use this boundary. See [security](SECURITY_MODEL.md).

Recovery must be classified honestly: reversible with specified prerequisites, compensatable with stated differences, irreversible, or unknown. Backup existence alone does not establish recoverability. Restoration needs its own verification, and rollback must not overwrite unrelated changes made since the original operation.

Execution and verification are separate dimensions. An execution can finish while verification fails or remains unknown. Outcomes distinguish no change, complete change, partial change, failure, and cancellation as applicable; verification records what was actually checked with **PASS**, **FAIL**, or **UNKNOWN**. A workaround must not be reported as a root-cause repair.

## Two faces

The AI interface may expose structured observations, capability evaluations, explanations, plans, and action results. The human interface exposes understandable explanations, comparisons, safe experiments, and controls referring to those same records. The human surface must disclose significant unknowns and the limits of return or undo.

Playground metadata is optional where a surface is technically unsuitable, but the engine must explain that limitation and expose a suitable inspection or reporting surface where reasonable. See [playground contract](PLAYGROUND_CONTRACT.md).

## Future conformance evidence

Conformance coverage should grow with actual capabilities. Observation and comparison examples should distinguish known absence from failed observation, irrelevant from required dependencies, and conflicting or stale evidence. When execution enters scope, add rejected out-of-scope action, changed preconditions, partial execution, and failed verification. Use synthetic fixtures before live mutation. The single next block is defined in [progress](PROGRESS.md); this list does not authorize implementing all cases at once.

Open questions include serialization, transport, identifier format, semantic version negotiation, and event persistence. This document deliberately leaves those choices unimplemented.
