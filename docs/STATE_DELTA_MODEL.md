# State, delta, and reconciliation

Status: **CONCEPT**. No state database, snapshot service, delta engine, or general rollback system exists in HAAEP Genesis.

The [Come-and-Go Law](COME_AND_GO_LEARNING.md) requires comparisons that retain knowledge when an experiment is reversed. The model must preserve uncertainty and distinguish observed state from desired state.

## Three responsibilities

| Responsibility | Input | Output | Boundary |
| --- | --- | --- | --- |
| State | Scoped observations | Identified snapshot with facts, evidence references, timestamps, scope, and omissions | A snapshot is not automatically a restorable backup |
| Delta | Two snapshots and explicit comparison rules | Comparable changes, unchanged observations, and incomparable or unknown fields | Difference is not proof of cause or improvement |
| Reconciliation | Objective, constraints, state, delta, and evidence | Explanation of agreement, conflict, uncertainty, and possible plan | Reconciliation proposes; it does not silently mutate |

Snapshots should identify their source, contract version, capture interval, platform or process context where relevant, and coverage. A multi-step observation may not be an atomic view of a changing system. Partial coverage must remain visible.

## Comparison semantics

Compare only fields with compatible identity, meaning, units, scope, and collection methods, or with an explicit evidenced conversion. The absence of a field in a snapshot may mean “not observed,” “unsupported,” or “redacted”; it does not automatically mean the resource disappeared.

Useful comparison outcomes include changed, unchanged within observed coverage, unknown, and incomparable. A transition from UNKNOWN to a known value is a change in knowledge; it does not by itself prove a machine change. Conflicting sources should remain distinguishable instead of being overwritten by the newest value without justification.

A delta records which snapshots were compared and the method used. Causal claims require additional evidence. Improvement requires a stated objective and verification; a newer runtime version is not automatically better for the current mission.

## Example learning cycle

1. Capture S0 for a bounded objective and record what was not observed.
2. Propose and authorize an experiment with expected effects and a recovery strategy.
3. Apply the experiment and capture S1 with execution and verification evidence.
4. Compare S0 and S1, including unrelated changes and gaps in coverage.
5. Continue, revise, or authorize supported recovery based on the objective and evidence.
6. If recovery occurs, capture S2 and verify the restoration claim. Preserve the experiment's lessons and its failed checks.

S2 need not be byte-for-byte identical to S0: logs, external services, elapsed time, or compensation may make exact restoration impossible. State the achieved restoration scope and remaining differences. Never silently erase a failed experiment to make history appear successful.

## Return and continuity

Before mutation, identify required backups, target identity, expected concurrent activity, and what can actually be restored. Recovery should not overwrite another actor's legitimate changes. Where restoration cannot be safely established, propose a narrower compensation or report it unavailable.

Events should correlate a mission, plan, grant, execution, observation, verification, and recovery attempt. These are semantic relationships, not a prescribed event-sourcing implementation. Retention, deletion requests, and privacy obligations apply to learning history; preserving knowledge does not authorize indefinite retention of secrets.

Sensitive payloads stay outside ordinary snapshots and logs. Store sanitized facts and limited evidence references with their access constraints. See [security](SECURITY_MODEL.md), [engine contract](ENGINE_CONTRACT.md), and the proposed [ARX relationship](ARX_RELATIONSHIP.md).

Storage technology, transaction boundaries, comparison formats, and retention policies remain open until a real engine and experiment supply requirements.
