# Agent workflow

A reusable way to coordinate Codex, Claude and other assigned workers: clear
ownership, bounded parallel work, independent testing and verified outcomes.
Use it with one human owner, one Project Lead, a builder and independent QA;
add specialists when they help. No particular model or application version is
required.

**Human → Project Lead → specialist or builder → independent QA → integrated
verification → authorized release.** This is an operating convention, not a
built-in requirement of any tool. The workflow does not grant access or approval.

## Start here

1. Read [the workflow](docs/workflow.md).
2. Follow [setup and project adoption](docs/setup.md) on a new machine or project.
3. Adapt the [project overlay](templates/PROJECT-OVERLAY.example.md) and record
   the exact shared commit your project reviewed. Read local instructions first;
   do not overwrite them or install global instructions.
4. Use the [bootstrap prompt](templates/BOOTSTRAP-PROMPT.md) for a read-only
   orientation, then assign the smallest useful task.

## Reusable templates

| Template | Purpose |
| --- | --- |
| [Project overlay](templates/PROJECT-OVERLAY.example.md) | Reviewed shared revision, local rules, checks and approval boundaries |
| [AGENTS entry point](templates/AGENTS.example.md) | Merge a short reference into existing project guidance |
| [CLAUDE entry point](templates/CLAUDE.example.md) | Give separately assigned builders the same project context |
| [Ownership map](templates/OWNERS.example.md) | Continuing owners, dependencies and shared-resource holders |
| [Task handoff](templates/HANDOFF.example.md) | Concrete assignment and verified delivery/progress |
| [Evidence receipt](templates/EVIDENCE.example.md) | Exact target, meaningful checks, integration and cleanup |
| [Deliverable index](templates/DELIVERABLES.example.md) | Private index across parallel projects: owner, evidence, next gate, three approvals, optional per-message approval |
| [Visual review example](templates/VISUAL-REVIEW.example.md) | Fictional controlled comparison: same framing, target-size checks, changed/unchanged |
| [Bootstrap prompt](templates/BOOTSTRAP-PROMPT.md) | Orient a new Project Lead without changing accounts or permissions |

Templates are examples until a project reviews and adopts them. Project names,
people, chat references, service accounts, runtime commands and release status
belong in that project's overlay and records. Keep them out of this shared guide.

Maintain general improvements through reviewed changes and the
[changelog](CHANGELOG.md); see [maintenance](docs/maintaining.md). A shared update
does not silently update projects or broaden their authority. Workloop is an
optional, separately supplied private dependency unless a destination project
requires it; its setup and feedback boundaries are covered in the setup guide.
