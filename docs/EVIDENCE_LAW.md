# Evidence Law

Status: **ADOPTED principle**. Evidence collection and action enforcement are **CONCEPT** during Genesis.

The required flow is **OBSERVE → EVIDENCE → UNDERSTAND → ACT → VERIFY**. When understanding or authority is insufficient, report the limitation and collect relevant evidence or propose a bounded next step. Do not guess and mutate everything.

## Evidence obligations

An observation should identify its source, collection time, scope, method, and limitations. Derived conclusions should identify the supporting observations and reasoning. Human explanations and machine-readable outcomes must preserve the distinction between direct observation, inference, and an untested hypothesis.

`UNKNOWN` is a valid outcome. Failure to observe a component does not establish that it is absent; seeing a version does not establish that the component is healthy; installation does not establish that the current mission requires it. Evidence can also become stale or conflict with another observation. Those cases require explicit treatment rather than a forced healthy/broken label.

## From evidence to action

1. Identify the human objective and the relevant environment boundary.
2. Gather only the evidence necessary to assess the problem, avoiding secrets.
3. Explain what the evidence establishes and what it does not.
4. Propose the smallest supported action, with risk, authority, and recovery limits.
5. Recheck relevant preconditions before acting; changed conditions can invalidate a plan.
6. Verify the intended result and report residual limitations or a failed verification.

An operation returning success is evidence that the operation ran; it is not by itself proof that the user's problem was repaired. A workaround must remain distinguishable from a verified root-cause repair.

## Example

A future adapter observes a runtime executable but cannot inspect its active environment. It may report presence with supporting evidence and active-environment status as `UNKNOWN`. It must not label the environment healthy or recommend reinstalling it solely because the second probe failed.

Synthetic fixtures and isolated experiments should test missing, conflicting, stale, and inaccessible evidence before a capability handles a live environment. The proposed [engine contract](ENGINE_CONTRACT.md), [ARX relationship](ARX_RELATIONSHIP.md), and [security model](SECURITY_MODEL.md) carry these obligations forward.
