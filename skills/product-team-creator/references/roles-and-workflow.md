# Example hierarchy and workflow skills

## Illustrative UltiStats organization

```text
Product section
  Product Owner
  Product QA (permanent integrated release acceptance)
  DevOps Lead (optional permanent infrastructure owner)
  Designer (optional permanent human design discussion)
Web section                         Backend section
  Web Lead                            Backend Lead
    issue worker → PR reviewer          issue worker → PR reviewer
```

This example contributes roles and relationships only. Product names, counts, repositories, model settings, sections, authority and cadence are interview decisions; never import live UltiStats IDs, runtime resources or historical policy holds into a new product. DevOps can own its temporary workers/reviewers; a Designer can coordinate small approved Web tasks with its lead. Keep existing current assignments when adopting a future-only workflow.

## Mandatory feature chain

1. PO and responsible leads use **task-scope-and-spec**: observable goal, scope/non-scope, testable requirements, unresolved decisions. This skill defines WHAT, not implementation ordering.
2. PO and leads use **task-coordination-strategies**: small acyclic dependency graph, owners, actual producer/consumer interfaces, earliest real end-to-end proof, ready frontier and merge sequence. Land checked prerequisites first; consumers use landed bases, not copied unmerged siblings. Avoid adding general infrastructure as a hidden dependency of a narrow product feature.
3. Each responsible lead **explicitly invokes to-tickets**, even if manual-only in the catalog. Supply agreed tracker and label configuration. Review the proposed breakdown at the delegated decision boundary; documented PO authority satisfies this, otherwise ask the human. Publish each approved leaf separately, with parent and actual blocking relationships. Keep parent acceptance distinct; no accidental closing references.
4. Each leaf has one independently verifiable outcome, scope, acceptance/checks, true blockers, intended landed base and diff estimate. Recommend <=1000 total added+deleted lines including tests/docs, with generated/binary changes shown separately. Record the chosen policy. Split complete behavior/responsibility; a genuine indivisible exception needs a concrete reason and bounded scope, not a blanket waiver.
5. Freeze the outcome; unrelated discoveries become new issues. Prompt actual availability callbacks advance consumers before routine timers. A checked leaf can merge without waiting for unrelated children or final release QA. Integrated QA and publication remain separate evidence stages.

## Task-specific skill routing

Load skills when their actual trigger applies; do not load the whole catalog into every worker. Their own instructions and the user's existing decisions still apply.

| Work | Skills to check/use when applicable |
|---|---|
| Initial PO/lead interview | grilling; team-lead-settings |
| Product/feature requirements and decomposition | task-scope-and-spec + task-coordination-strategies; lead to-tickets |
| Nontrivial design choices / implementation sequence | superpowers:brainstorming; superpowers:writing-plans |
| Isolated development / implementation / defects | superpowers:using-git-worktrees; superpowers:test-driven-development; superpowers:systematic-debugging |
| Independent PR review and fix replay | superpowers:requesting-code-review; superpowers:receiving-code-review |
| Evidence and branch completion | superpowers:verification-before-completion; superpowers:finishing-a-development-branch |
| DevOps pipeline / actual GitHub Actions failures | deployment-pipeline-design; gh-fix-ci |
| UI design / accessibility / Figma / raster assets | frontend-design; web-design-guidelines; relevant Figma skills; imagegen |

Only the setup and mandatory feature-chain skills are unconditional dependencies of this skill. For any other skill actually invoked, verify it and follow the missing-skill installation protocol. Do not fabricate a substitute or add speculative setup gates. Respect established autonomy; avoid asking the same human decision in several roles.
