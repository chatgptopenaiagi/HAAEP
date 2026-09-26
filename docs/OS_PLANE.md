# Operating System Plane

Status: **CONCEPT / RESEARCH DIRECTION**. HAAEP implements no operating-system adapter and advertises no Windows, WSL, Linux, or macOS runtime support.

Windows is the strongest evidenced starting environment because of the independent CWRE case studies and the Genesis development environment. That experience supplies requirements and lessons; it is not a HAAEP support certification.

## Adapter direction

Possible future adapters are Windows, WSL, Linux, macOS, and other operating environments when real requirements justify them. Each should explain the facts and capabilities observable in its own execution context.

Candidate concerns include identity, privilege, command resolution, environment scope, filesystem behavior, processes, services, security context, and relevant runtime access. A common fact vocabulary should emerge from actual adapters and conformance cases. Genesis does not define a universal OS interface that pretends these systems are interchangeable.

| Environment | Distinctions that future evidence may require |
|---|---|
| Windows | Token and integrity context, UAC, command aliases, PATH, process inheritance, permissions |
| WSL | Distribution and guest identity, host/guest boundary, path translation, device availability, separate process contexts |
| Linux | UID/GID, capabilities, sudo context, namespaces, service context, relevant security policies |
| macOS | User and privilege context, sandboxing, application trust, service-launch context |

These are investigation topics, not implemented probes or exhaustive descriptions. An elevated process is not automatically entitled to perform every available action. HAAEP authorization remains a separate decision from OS capability.

## Normalization boundary

Normalize only claims that share tested semantics. Retain platform details needed to explain differences. “Can perform this named operation in this context” is often more useful than forcing every platform into a single administrator boolean.

An unavailable probe, denied observation, unsupported environment, or unknown output shape should remain explicit. Facts from the Windows host must not stand in for facts from a WSL guest or container. A path must carry the environment in which it has meaning.

## Support gate

A supported adapter needs a bounded stated capability, an identified environment matrix, reproducible fixtures, task-relevant live evidence, and documented limitations. Tests on one host do not justify platform-wide support claims. Cross-platform promises require real second-platform evidence and verified contract behavior.

A future first block should inspect a narrow Windows requirement without mutating global configuration. WSL and native Linux expansion should follow actual missions rather than an arbitrary parity checklist. Security-policy changes, service changes, and persistent environment edits require their own plans and authorization.

See [CWRE relationship](CWRE_RELATIONSHIP.md), [security model](SECURITY_MODEL.md), [runtime plane](RUNTIME_PLANE.md), and [roadmap](ROADMAP_2_YEARS.md).
