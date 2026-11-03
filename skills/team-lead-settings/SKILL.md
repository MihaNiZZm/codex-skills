---
name: team-lead-settings
description: Use when creating or reconfiguring a repository team lead, including worker concurrency, worktrees, PR reviewers, chat callbacks, timers, or stop and archive policies.
---

# Team Lead Settings

Configure one repository team with explicit ownership and a durable operating agreement. Reuse existing decisions and chats; setup does not start a feature automatically.

## Dependencies

**REQUIRED SUB-SKILLS:** `grilling`, `task-scope-and-spec`, `task-coordination-strategies`, `to-tickets`. Check their actual availability before invocation. An installed skill absent from the catalog may be read at its verified local path. If missing, follow [dependency installation](references/dependency-installation.md); report the missing name and installation steps, then continue unaffected preparation.

## Configure the lead

1. Discover existing lead/PO/peer chats, repository instructions, local checkout, remote, target branch, tracker and current assignments. Use actual app capabilities; do not invent chat APIs or claim creation from a plan.
2. **Use `grilling`** to resolve the current independent decision frontier, with recommendations. Read [intake and configuration](references/intake-and-configuration.md). Honor supplied answers; ask only unresolved choices, then confirm the concrete configuration before applying it. A confirmed standing policy authorizes its routine future steps without another general ACK.
3. Persist the agreement and primary human decision references in the project's coordination location. Resolve the checkout/concurrency invariant before creating workers. Apply only the agreed settings, preserving active PR assignments unless explicitly changed.
4. Read back actual chat/section/repository/timer identities and report configured versus still pending. Save the lead's bootstrap instructions with its parent and peer contacts, skill names, policies and state path.

## Required operating rules

| Decision | Contract |
|---|---|
| Parallel development | Separate worktree/branch per active worker; prerequisites based on landed code. |
| One shared checkout | **One active development/validation task at a time.** Disjoint files or serialized Git commands do not permit parallel workers. If four workers are requested here, ask worktrees versus sequential execution before dispatch. |
| Feature decomposition | PO and lead use `task-scope-and-spec` for WHAT and `task-coordination-strategies` for dependencies/ownership. Lead then explicitly invokes `to-tickets` for small verifiable child issues. |
| Ticket agreement | Supply configured tracker/labels to `to-tickets`. Its breakdown review is with the authorized decision maker: PO under documented delegation, otherwise human. Do not invent a setup-skill prerequisite when tracker configuration is already provided. |
| PR ownership | One leaf outcome per PR, explicit parent/prerequisites, acceptance checks, intended base and diff budget; unrelated work becomes another issue. |
| Independent review | Apply selected shared or per-PR mode. Dedicated reviewer starts after first working PR; same reviewer follows corrected heads through checked merge. |
| Callback | Use authorized routes and concrete events; durable evidence and next owner accompany handoffs. Receive-side requests alone do not grant send authority. |
| Completion | Actual checked merge plus owned runner/resource/lease END precedes temporary chat archival. Preserve source/evidence; remove that chat's finite timers. Permanent lead and Product QA persist. |

## Common mistakes

- Four workers in one tree: resolve isolation first; file ownership is insufficient.
- Treating `to-tickets` as unavailable because it is manual-only: this workflow explicitly directs the lead to invoke it.
- Creating a fresh reviewer to retry a platform-blocked action: reviewer policy does not authorize circumvention. Finish unrelated work and report the precise block.
- Inferring deployment, protected-resource changes or recipient callbacks from role creation: retain explicit authority boundaries.
