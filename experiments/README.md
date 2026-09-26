# Experiments

Status: **RESERVED boundary; no experiments executed by Genesis**.

Experiments test an architectural uncertainty or observed engineering problem.
They do not turn roadmap entries into product support claims. Prefer synthetic
fixtures, temporary workspaces, and bounded simulations before live integration.

A future experiment should record:

- The question, evidence, hypothesis, objective, and stopping condition.
- Inputs and provenance, with synthetic data explicitly labeled.
- Authorized scope, permissions, expected effects, and recovery limitations.
- Method, focused validation, actual outcomes, uncertainty, and comparison.
- Retained learning and whether an existing decision is supported or superseded.

Keep private machine data outside Git; sanitized exports still need review.
Fixtures intended for sharing belong in the experiment only when synthetic or
explicitly reviewed. An ignored `.local/` directory can hold local disposable
working artifacts, but is not a secret storage system.

The single scheduled next block lives in
[PROGRESS](../docs/PROGRESS.md), not in a competing experiment backlog. Follow
the [mission template](../missions/MISSION_TEMPLATE.md),
[Evidence Law](../docs/EVIDENCE_LAW.md), and
[state/delta model](../docs/STATE_DELTA_MODEL.md).
