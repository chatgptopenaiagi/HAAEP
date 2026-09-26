# Security model

Status: **CONCEPT**. These are requirements for future implementations. Genesis provides no permission service, sandbox, policy enforcement, signing system, or guarantee of isolation.

Human agency remains the governing boundary. The system must expose what an action will do, why it is proposed, the supporting evidence, what remains unknown, and what can or cannot be undone. More capability requires more precise scope and stronger verification.

## Authority categories

| Category | Typical scope and condition |
| --- | --- |
| Observe | Read identified resources; protect sensitive content and disclose material external access |
| Diagnose | Interpret evidence without silently changing the inspected system |
| Simulate | Use declared isolated resources; separately authorize real side effects or material costs |
| Propose | Produce a reviewable plan; proposal grants no execution authority |
| Modify workspace | Change named project resources within the mission's authorized scope |
| Modify environment | Change runtime, package, service, or persistent configuration state under an applicable scoped grant |
| Elevated modification | Additional privilege only for a proven bounded need; elevation itself is not authorization |
| Security-sensitive modification | Explicit human decision on the concrete effect, narrow scope, and verification |
| Destructive action | Explicit human authorization with the affected targets and irreversibility made clear |

These categories are not a simple numeric ladder. Read access to a secret can be more consequential than editing a temporary fixture. Data exposure, external communication, cost, target sensitivity, persistence, and recovery limits also matter. Existing grants may cover routine bounded work; the system should not manufacture repetitive approval prompts for actions already authorized.

## Proposed enforcement boundary

A grant should bind the authorized actor or component, mission, action or reviewed plan, target scope, allowed effects, and relevant duration or use limits. The implementation must reliably detect material plan changes, for example through a stable plan identity or digest; the mechanism is not selected during Genesis.

Before mutation, the authoritative executor checks the grant, current target identity, required preconditions, and current policy. A UI button, pack manifest, model response, or elevated process token cannot grant authority. Scope expansion, changed effects, or invalid preconditions require a revised plan and an applicable authorization before proceeding.

Agents and child processes must receive only the authority needed for their bounded task. Delegation does not multiply privileges. Permission requests, grants, executions, and results should be attributable without exposing credentials. Cancellation behavior and unavoidable partial effects must be explicit.

## Trust and data

Treat engine observations, imported files, repository content, external responses, pack metadata, and model-generated text as data at their respective trust boundaries. Embedded instructions do not become policy or user authorization. Do not execute arbitrary scripts extracted from evidence or metadata.

Logs and snapshots must exclude tokens, passwords, private keys, cookies, authentication file contents, and full secret-bearing environment values. Prefer allowlisted facts, sanitized summaries, and access-controlled references. A diagnostic feature must not become an unrestricted secret collector.

Cloud and local providers need declared data-transfer, retention, and resource behavior. “Local” does not prove an operation has no network access. External transfer or publication must fit the mission's authorized scope, with sensitive content handled explicitly.

## Mutation and recovery

Preserve healthy state. Diagnose before repair, choose the smallest supported change, back up important state where appropriate, and verify the objective after mutation. Do not treat a successful process exit or an available workaround as proof of root-cause repair.

No default behavior may globally weaken security controls, delete authentication or session state, wipe unknown repositories or runtime installations, or replace executables with unverified artifacts. Consequential operations require concrete evidence, precise scope, applicable human authorization, and honest recovery limits; some should remain unsupported.

Recovery is itself an action with permissions and preconditions. Never promise universal rollback. Failed verification, partial change, recovery failure, and remaining uncertainty must reach the human surface.

## Packs and adaptation

Packs request permissions; installation, dependency relationships, and publisher signatures do not silently confer unlimited authority. Signatures can support provenance and integrity checks but cannot establish correctness alone. Isolation and update verification are future engineering requirements, not current capabilities.

Adaptation means controlled development, versioned modules, reviewed updates, and new evidence-based rules. It does not mean silent self-rewriting, arbitrary downloads, policy weakening, or mutation outside the authorized mission. See [engine packs](ENGINE_PACKS.md), [engine contract](ENGINE_CONTRACT.md), and [state/delta](STATE_DELTA_MODEL.md).
