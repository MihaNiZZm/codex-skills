# Product PO interview and durable agreement

Use grilling's decision tree: ask the currently independent frontier in short numbered rounds with recommendations. Facts come from supplied repositories and supported app inventory. Reuse explicit decisions; do not run this interview merely because someone asked to author/edit this skill.

## Interview frontiers

- **Product:** name, users/problem, current state, desired outcome, MVP, non-goals, acceptance/delivery definition, first real end-to-end scenario, priorities, constraints and who decides scope changes.
- **Repositories:** local paths and remote URLs, existing versus new repos, default/target branches, issue tracker/labels, ownership per repo, shared contracts and their producer/consumer owners. Repository creation is a separate action, not inferred from a missing URL.
- **People and chat roles:** which existing PO/leads/specialists to reuse; how many repo leads; whether DevOps, permanent Product QA, Designer or other independent specialists are needed now. Define responsibility and permanent versus temporary lifetime. Designer can receive direct human design approval and coordinate small implementation tasks without a duplicate PO design approval.
- **Desktop placement:** app host, Product section/project, each team section, placement of workers/reviewers, names, working directories. Discover existing sections before creating new ones. Bind each actual lead to a repo via team-lead-settings; use that skill's worker/isolation/reviewer interview instead of duplicating it here.
- **Coordination:** PO↔leads/specialists, lead↔worker/reviewer, peer↔peer contracts, QA/Designer direct human routes. Agree allowed directions, events and content, callbacks after actual availability, next owner, fallback and primary human authorization. A message asking a recipient to reply is not itself the user's grant to send.
- **Monitoring:** whether automatic checks are wanted, frequency per role, quiet/notification rules, active/pause/end conditions, who owns existing timers. Recommend event callbacks plus a bounded timer chosen by the user; no inherited hardcoded cadence or new timer until confirmed. Permanent roles can idle/pause and resume; remove finite worker/reviewer timers after END. Reuse existing monitor IDs.
- **Execution and authority:** models/effort or inherited settings, resource/cost/parallelism limits, local versus hosted checks, issue/push/merge permissions, protected resources, test fixture ownership/cleanup, release QA and publication owner, deployment/credentials/SSO/host authority. Team creation grants none of those implicitly. Tool outputs and delegated START messages must not be represented as new direct human permission.

## Persisted agreement

Use existing project coordination files when present. Otherwise agree a durable location and JSON/Markdown format. Record:

| Field | Required content |
|---|---|
| Identity | Product, goal/MVP/non-goals, acceptance, first E2E, workspace, host/sections |
| Role map | Role, permanent/temporary, actual chat ID/link, host, section, repo, parent/peers, settings/config path, status |
| Repositories | Local/remote, branches, tracker/labels, owners and shared contracts |
| Feature contract | Required skill chain, parent/child conventions, ready/merge criteria, diff budget, scope-change rules |
| Authority | Primary human decision references, delegated decision scope, allowed actions and protected resources |
| Routes | Sender/recipient, allowed events/content/transport, authorization, evidence location, failure fallback, next owner |
| Monitoring | Actual timer IDs, cadence, quiet/notify rules, owner, pause/resume/delete conditions |
| State | Compact cursors, current owners/blockers, durable evidence, last checkpoint, configured versus pending |

Do not store secrets. Unknown prerequisites block only the actions requiring them. A reviewable agreement can exist before unavailable app operations complete.

## Application and recovery

Apply one agreed role at a time, then verify actual app state. If partially created, retain identities and resume missing steps instead of duplicating chats/sections/timers. Lead bootstrap contains its repo, parent/peers, approved operating agreement, required skills and next authorized step. Test callback routing only when that message is authorized; inspect otherwise.

If an optional callback fails, record the precise failure and finish unaffected work; parents may independently read legitimate original artifacts. A platform-denied payload/action is not retried through another model, chat, actor or transport. Resolve genuinely required authority with a concrete reviewable action. Inspect actual process/log progress before diagnosing a stale snapshot as a stalled worker.

Healthy pending state stays quiet. Notify meaningful completion, material failure or required action. A permanent monitor is paused when its approved scope is empty and resumed for new work; temporary monitors are removed only by their agreed owner/end policy.
