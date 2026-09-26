# Instructions for HAAEP development sessions

HAAEP is a long-term architecture project. Finish one coherent, evidence-backed
block per session. Do not implement a capability merely because the roadmap
names it. The working name may change without changing the product law.

> Build complexity for AI, but always return an understandable, explorable and controllable world to the human.

## Session start

1. Confirm the actual repository root, branch, remotes, and working directory.
   Never assume a historical path or use a shell installation folder as a project.
2. Read [docs/MISSION.md](docs/MISSION.md) and [docs/PROGRESS.md](docs/PROGRESS.md).
3. Read applicable entries in [docs/DECISIONS.md](docs/DECISIONS.md), then inspect
   Git status. Preserve unrelated local work; do not reset or clean it away.
4. Read affected architecture and contract documents. Treat conceptual contracts
   as proposals requiring evidence, not as implemented APIs.
5. Run existing focused tests when relevant code exists. When it does not,
   validate the affected documentation and explicitly report that limitation.
6. Find `NEXT_EXACT_ACTION`. Follow it unless the current human mission changes
   scope; record an intentional change instead of silently expanding the block.

## During the block

- Follow discover → model → implement → test → verify → document → preserve.
- Preserve Caesar, Playground, Chocolate, Engine, Come-and-Go, and Evidence
  principles. Both planes use one authoritative engine meaning and permission
  boundary. Human interfaces must make consequential choices understandable.
- Observe before acting. Preserve unknown, scope, provenance, and evidence
  freshness. Distinguish presence, health, task necessity, and capability.
- Define expected results and verification before mutation. State whether return
  is exact restoration, compensation, partial, unavailable, or unknown; do not
  promise universal undo. Preserve evidence after a return.
- Keep permission to inspect, propose, simulate, and execute separate. A pack,
  agent, model, or playground does not inherit unlimited authority. Explicit
  current user authorization governs the current scope; do not repeatedly ask
  for authorization already granted.
- Test with synthetic fixtures and temporary workspaces when possible. Never
  damage the live machine to demonstrate recovery or invent successful checks.
- No secrets, tokens, authentication files, raw private environment dumps, or
  sensitive machine snapshots in Git or ordinary logs. `.gitignore` is only an
  aid; inspect the actual staged changes. Use synthetic, labeled examples.
- CWRE and other specialist projects remain external. Do not rename, merge,
  mutate, or import their source as part of HAAEP work without an explicit new
  scope. Read architectural lessons narrowly when needed.
- Do not add uncontrolled self-modification, silent security weakening, arbitrary
  code download/execution, or speculative module implementations.
- Record substantive architectural choices by appending ADRs. Supersede earlier
  decisions explicitly; do not silently rewrite history.
- Use capability status labels honestly: `CONCEPT`, `PLANNED`,
  `RESEARCH DIRECTION`, `PARTIAL`, `IMPLEMENTED`, `VERIFIED`. Verification always
  has a scope, environment, and date; it does not imply universal support.

## Finish and hand over

1. Complete appropriate focused validation; report observed results and limits.
2. Update affected documentation and `docs/PROGRESS.md`, including block history,
   limitations, and **exactly one bounded `NEXT_EXACT_ACTION`** with acceptance
   criteria. Do not turn it into a second roadmap.
3. Review the diff and staged file list, then make one or a small number of
   coherent commits. Do not commit unrelated work or private evidence.
4. Push when appropriate and authorized. Genesis explicitly authorizes creation
   and publication to the authenticated account as a private repository.
   Later missions should use their current authorization and repository policy.
5. If publishing, verify owner, repository, visibility, branch, remote commit,
   expected files, and working tree status. Report any remaining changes honestly.
6. Stop when the bounded block is complete. Leave the next block to the next
   session rather than executing the roadmap indefinitely.

## Genesis-specific boundary

The Genesis deliverable is documentation and Git/GitHub foundation only. No
runtime, GUI framework, package manager, plugin loader, installer, or application
test framework is selected by this mission. Licensing remains pending and initial
visibility is private until an explicit owner decision supersedes it.
