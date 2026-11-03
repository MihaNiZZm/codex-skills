---
name: product-team-creator
description: Use when setting up or onboarding a product organization in the desktop app with a Product Owner chat, repository team leads, independent specialists, and cross-chat coordination, or when configuring an existing product team hierarchy.
---

# Product Team Creator

Bootstrap a product organization through its own PO chat. Establish a concrete operating agreement before creating its teams; reuse existing roles and decisions.

## Dependencies and capabilities

**REQUIRED SUB-SKILLS:** `grilling`, `task-scope-and-spec`, `task-coordination-strategies`, `to-tickets`, `team-lead-settings`. Verify installed copies; read verified paths when the catalog has not refreshed. For missing skills, name them and give [installation instructions](references/dependency-installation.md). Continue unaffected preparation; do not silently replace a missing skill.

Discover actual desktop tools for inventory, chat creation/placement, settings, messaging and timers. If capabilities are missing, prepare the configuration and explain the required app/plugin or manual step; never claim chats or monitors were created.

## Bootstrap in two stages

1. **Find placement.** Inventory relevant existing chats/sections and the supplied workspace. Resolve only missing minimum product identity, PO location/working directory and whether to create or reuse the PO. Repository/team composition and timer decisions belong in the PO interview. Use an existing current PO when configuring an existing product; do not create a duplicate.
2. **Open the authorized PO.** Create/reuse that chat with the bootstrap contract below. The detailed **`grilling` interview happens in this PO chat**, in rounds of the current independent decision frontier. Use [intake and agreement](references/intake-and-agreement.md); honor prior answers. Other chats/timers wait for the agreed role map and settings. Do not copy another product's IDs, cadence or permissions.
3. **Apply the confirmed agreement.** Show the concrete hierarchy, repo ownership, callback routes, authority and timer settings for confirmation. Prior explicit approval of that exact configuration counts; avoid repeated general permission gates. Persist configuration and primary human decision references. Configure each lead using `team-lead-settings` before workers start. Create only selected roles, with agreed lifetime and section.
4. **Verify and hand off.** Read back actual identities, placement, repository settings and timer IDs; record configured/pending state and the next owner. Setup creates no feature tickets, workers, deployment or repository changes unless separately included in the authorized scope.

## PO bootstrap contract

Supply product identity, configuration path, known decisions, human authority references and authorized chat routes. Direct the PO to:

- Conduct `grilling` for product, team, collaboration and monitoring decisions; keep discovered facts separate from unresolved choices.
- For **each future feature**, work with its leads using `task-scope-and-spec` (WHAT/acceptance), then `task-coordination-strategies` (small dependency graph, ownership, early real integration). **Leads explicitly invoke `to-tickets`** to publish agreed small verifiable child issues. Preserve its breakdown agreement with the human or documented PO delegate.
- Maintain parent project/issue → independently testable child → one PR per child. Agree diff budgets, actual prerequisites and merge boundaries before dispatch; do not expand parent work into one giant PR.
- Send prompt authorized availability/blocker callbacks with evidence and next owner. Timers are a safety net, not a prerequisite to starting ready work.
- Distinguish source checks/merge, owned runtime proof, integrated Product QA, PO acceptance and actual delivery. Keep permanent roles; archive temporary workers/reviewers only under their agreed END rules.

For an illustrative hierarchy and task-specific skill routing, read [roles and workflow](references/roles-and-workflow.md). Treat examples as options, never as product requirements.

## Common mistakes

Creating every example specialist, copying timers, interviewing everything before opening the PO, or retrying a platform-blocked action through a new chat all violate this setup contract. Role creation does not grant deployment, billing/host changes or new cross-chat messaging authority.
