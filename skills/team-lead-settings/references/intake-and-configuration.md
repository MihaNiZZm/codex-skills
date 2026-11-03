# Lead interview and saved configuration

Use grilling in rounds of currently answerable questions, not one giant questionnaire. Discover repository facts before asking. Offer recommendations and accept existing explicit choices.

## Decision frontiers

1. **Ownership:** Which exact local/remote repository, default/target branches and tracker does this lead own? Who is the parent PO, merge integrator, contract owner and relevant peer? Reuse which existing chats and desktop section? What is outside this team's scope?
2. **Execution:** How are workers created (desktop task chats versus another explicitly supported mechanism)? Which model/effort/default settings? How many simultaneous workers and heavy jobs? Recommend separate worktrees for parallel work. A shared checkout sets active development/validation concurrency to one, including review commands that mutate/build there. A read-only reviewer can use an immutable snapshot without sharing mutable runs.
3. **Review:** Shared independent reviewer or one dedicated chat per PR? Recommend per-PR after the first working version, with a separate worktree/context and same reviewer for fixes. Specify who merges, required checks, local/hosted CI policy and how review evidence binds to the actual head. In shared mode keep the reviewer while its queue/role exists; do not archive it after every PR.
4. **Lifecycle and coordination:** Which events/routes may worker, reviewer, lead, PO and peers send directly? Who handles unavailable recipients and optional failed callbacks? Which chats stop/archive when, and who releases their resources and removes finite watchdogs? Permanent roles remain. Distinguish source closure from integrated release QA, PO acceptance and delivery.
5. **Autonomy and monitoring:** May this lead create issues/PRs, push, merge and provision owned test resources under what limits? Production deployment/credentials/host operations need their own authority. Are timers wanted for lead/worker/reviewer; at which cadence, quiet conditions and pause/resume/end rules? Recommend event-driven handoffs plus bounded monitoring. Reuse timer IDs; never create monitors merely because this skill runs.

## Required saved fields

Use the repository's existing JSON/Markdown format. Each field has a confirmed value, an explicitly accepted default, or `pending`; a pending prerequisite blocks only the affected action.

- Product/team name; lead thread/host/desktop section; parent PO and peer identities.
- Local/remote repo, target/base branches; tracker, label vocabulary, parent issue/project conventions.
- Skill names/resolved locations; primary human decision references and any delegated decision authority.
- Worker creation mechanism/model/effort, development isolation, max active workers and heavy-job limits.
- Reviewer mode/settings, first-PR trigger, independence, same-reviewer replay, merge owner/checks.
- Small issue contract: outcome, scope/non-scope, acceptance, verification, true blockers, landed base, producer/consumer owner, estimated added+deleted lines including tests/docs. Suggest <=1000 total as a starting guideline; record the chosen limit. An indivisible exception needs a concrete reason and bounded scope before expansion.
- Callback matrix: sender, recipient, authorized events/content, source of human authorization, transport, durable fallback, next owner. No secrets in prompts/logs.
- Timers: role, existing/new ID, cadence, owner, notify conditions, pause/resume/removal conditions.
- Worker/reviewer END and archive policy; evidence/worktree retention; permanent roles.
- Release QA and publication responsibilities; protected resources and authority limits.

## Bootstrap contract

A lead prompt contains: owned repo/section + parent/peers + configuration path + required skills + next authorized step. For each future feature, produce specs with PO, validate a small acyclic graph, then invoke to-tickets and work only its ready frontier. Preserve to-tickets' breakdown agreement step; documented PO delegation can satisfy it. Its missing-tracker setup suggestion is unnecessary when this configuration supplies tracker and labels. Retain parent issues until their actual acceptance; use parent references, not accidental closing references.

A handoff contains: issue/PR, exact head and verification result, evidence location, available interface, owned resource/lease status, unresolved blocker, next action and owner. A source merge should promptly unblock its consumer; do not wait for a periodic timer or whole-release QA. Source checks, process/fixture checks, integrated QA and delivery are distinct statuses.

If a callback fails, record it and continue unaffected authorized work. The parent may independently inspect legitimate original artifacts. Do not relay a denied payload through another actor/transport or manufacture authorization. Inspect actual process/log progress before restarting an apparently stale worker; preserve original failure evidence.

## Example

Web lead owns one repository, uses two worker worktrees and one reviewer per PR. PO and lead agree a narrow behavior and dependency graph; lead invokes to-tickets to publish approved child issues. Worker A's checked prerequisite merges and reports actual availability to lead and authorized consumer B. A and its reviewer archive after owned END; B starts from the landed prerequisite. Product QA later verifies the integrated candidate.
