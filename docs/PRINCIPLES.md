# HAAEP principles

Status: **ADOPTED architectural guidance**. Genesis establishes these laws in documentation; it does not implement their enforcement.

> Build complexity for AI, but always return an understandable, explorable and controllable world to the human.

HAAEP exists to connect human intent with AI engineering capability. A simpler human experience must preserve access to evidence, uncertainty, consequences, and choice. Complexity may be hidden from the first view; consequential behavior must remain inspectable.

## Five major principles

| Principle | Architectural obligation |
| --- | --- |
| [Caesar Principle](CAESAR_PRINCIPLE.md) | Give computation to machines while preserving human purpose, interpretation, responsibility, authorization, and final choice. |
| [Playground Law](PLAYGROUND_LAW.md) | Important, technically suitable capabilities should expose a useful, safe human surface for observation and experimentation. |
| Engine Law | Grow through coherent engines, adapters, packs, and contracts. Keep engine logic independent of a particular GUI and authoritative across both planes. |
| [Come-and-Go Law](COME_AND_GO_LEARNING.md) | Compare states, return when useful and possible, and retain the knowledge learned from the experiment. |
| [Evidence Law](EVIDENCE_LAW.md) | Observe, collect evidence, understand, act, and verify. Insufficient evidence remains `UNKNOWN`. |

The **Chocolate Rule** accompanies the Playground Law: when AI performs difficult engineering work, it should, where technically reasonable, return a simple, useful, enjoyable way for the human to experience the result. The informal name does not reduce the requirement's seriousness.

## Engine Law in practice

An engine owns a coherent engineering responsibility. Adapters translate environment-specific behavior; packs group related capabilities; playgrounds expose them to humans. These roles are connected through [engine](ENGINE_CONTRACT.md), [pack](ENGINE_PACKS.md), and [playground](PLAYGROUND_CONTRACT.md) contracts.

The AI interface and human interface consume the same engine semantics. A UI must not implement a second diagnosis, authorization system, or repair algorithm. A machine interface must not bypass authorization just because no GUI is involved.

New boundaries should answer a real requirement. Naming a possible engine does not justify implementing it, and a future catalog entry is not a support claim.

## Applying the laws

Every development block follows **DISCOVER → MODEL → IMPLEMENT → TEST → VERIFY → DOCUMENT → PRESERVE → NEXT EXACT ACTION**. Preserve healthy state, prefer narrow changes, and expose limitations. Adaptive growth means controlled, versioned development; it does not permit uncontrolled self-modification.

When principles appear to conflict, document the tradeoff and preserve human agency, evidence, and the [security boundary](SECURITY_MODEL.md). A convenient control cannot justify an unbounded action; an attractive diagram cannot substitute for a verified result.
