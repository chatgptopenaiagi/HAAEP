# Come-and-Go learning

Status: **ADOPTED principle**; state capture, comparison, and recovery mechanisms are **CONCEPT**.

Intelligence should not be modeled only as forward execution. Returning with preserved knowledge is learning, not failure.

```text
STATE A → bounded experiment → STATE B → compare with objective
                                          |
                       +------------------+------------------+
                       |                                     |
                    continue                        return when useful
                                                             |
                                                    retain knowledge
                                                             |
                                                     new experiment
```

## What an experiment should preserve

Before acting, identify the objective, relevant baseline, expected observations, authority, and recovery limits. After acting, preserve what was attempted, what changed, verification evidence, and what remains unknown. A return must not erase the reasoning or evidence needed to learn from the attempt.

Returning is not necessarily restoring the entire machine. It may mean reverting one workspace change, selecting an earlier design, or restoring a verified configuration backup. Some operations are irreversible, some need a compensating action, and some have no known recovery method. An engine must declare that distinction before consequential execution.

## Comparison rules

- Compare states with compatible scope, schema, and observation context; otherwise label the comparison limited or unknown.
- Separate an observed difference from a causal explanation. A change after an action does not alone prove that action caused it.
- Evaluate against the stated objective; a numerically larger value is not automatically an improvement.
- Verify a return independently and report partial or failed restoration.
- Retain sanitized evidence according to explicit retention rules. Preserving knowledge does not justify preserving secrets indefinitely.

A future synthetic runtime experiment could compare two proposed task environments without altering either installed runtime. If the proposal performs worse against the selected requirement, the user can retain the original choice and the comparison evidence. This is a conceptual example, not a Genesis experiment implementation.

See the [state/delta model](STATE_DELTA_MODEL.md), [Evidence Law](EVIDENCE_LAW.md), and [playground contract](PLAYGROUND_CONTRACT.md).
