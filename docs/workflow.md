# The workflow

Start from the human's intended outcome and accepted decisions. Assign the work
needed to achieve it, verify the actual integrated result, and report what is
still open. A message, checklist or artifact alone does not prove the outcome.

## Ownership

| Role | Owns | Evidence of completion |
| --- | --- | --- |
| Human owner | Product decisions, priorities and action-specific authorization | Recorded decision and scope |
| Project Lead | Original outcome, dependencies, assignments and final reconciliation | Inspected result and explicitly owned open items |
| Specialist | One continuing area, such as design, operations or measurement | Usable deliverable and relevant integration checks |
| Builder | Assigned implementation and meaningful regressions | Exact source/build, checked diff and test evidence |
| Independent QA | Acceptance of a stable target, reproductions and test gaps | Per-case results, evidence and limits |
| Release owner | Reviewed integration and authorized release | Final source, deployment or delivery identity, live result and cleanup |

A builder's own pass is not independent QA. QA acceptance is not permission to
merge, deploy, send messages, change live settings or spend money. Use existing
applicable authorization without asking again unnecessarily, but record its
actual scope. Titles and this guide grant none. If an operation needs approval,
prepare a concrete reviewable result first and identify the exact remaining
boundary.

Use three worker types deliberately:

- **Persistent named chats** own ongoing areas and durable records. Inspect their
  current assignments and workload before dispatching more. Create new chats
  when the human requests or explicitly authorizes them; do not duplicate an
  existing owner.
- **Temporary subagents** handle bounded parallel work inside an assigned task,
  such as a source review or independent check. They report to their parent;
  they do not replace continuing owners or extend the task's authority.
- **Claude sessions and other builders** are separately assigned workers. They
  may not appear in the same chat inventory. Use a written handoff and verified
  response. An old worktree is not proof of an active session, and editing a
  document does not deliver an assignment.

## Run one task

1. **Define the outcome and dependencies.** Preserve the original request and
   accepted changes. Give each necessary dependency an execution owner, next
   action and acceptance evidence. Label an assignment as action, documentation
   or context. A coordination note must not substitute for implementation.
2. **Dispatch and verify delivery.** Check the intended recipient, current work
   and target version. Use an authorized channel and retain its dispatch
   receipt. **Sent** means accepted dispatch; **Acknowledged** means the
   recipient addressed this scope; **Started** means the requested work began;
   **Completed** means the deliverable and checks were inspected. If delivery is
   disputed, inspect the recipient and response before resending. Use the
   [handoff template](../templates/HANDOFF.example.md).
3. **Prepare the change under local policy.** Read the project's instructions
   and chosen spec/plan process. Some projects require spec → complete-code
   plan → implementation and byte-for-byte plan/source comparison before merge;
   others do not. Record the adopted convention in the overlay. Do not impose
   a former project's rules or waive a destination project's requirements.
4. **Make a meaningful reproduction for a bug.** Freeze the matching baseline,
   expected failures, positive controls and behavioral checks. Use the approved
   bug-fix workflow; where Workloop is required, follow its installed skill and
   current routing. Never reuse an unrelated starter or weaken an assertion
   merely to accept a fix. Preserve actual reports/diffs, test-contract changes
   and review disposition.
5. **Freeze and independently verify.** Record commit, dirty-source hashes if
   any, served build, environment, relevant configuration and fixtures. Notify
   QA if the target changes. Use pass/fail/blocked/not-run, exact steps and
   explicit limits. Distinguish unit/local, browser emulation, actual browser or
   device, provider readback and human-observed evidence. A DOM assertion is
   not audible screen-reader verification; a tagged URL is not proof that
   reporting received a visit. See the [evidence template](../templates/EVIDENCE.example.md).
6. **Integrate and release within authorization.** Bring in current upstream
   work, preserve concurrent changes and resolve overlaps. Compare the final
   source with what QA tested. Rerun affected checks and all required release
   checks; obtain independent disposition on the final target. When authorized,
   record publication, merged tree, deployment or delivery identity, actual
   outcome and cleanup separately. A merged PR is not a verified deployment.

Finally inspect the deliverable in its intended context against the original
request, not just the latest handoff. Separate completion from limits: for
example, “design complete; integration assigned; physical proof pending.” Do not
close a dependency because somebody documented or acknowledged it.

## Parallel work without collisions

Use an isolated checkout for each concurrent source-writing task. Inspect
worktree inventory and reuse a suitable owned checkout before creating another.
Worktrees have separate working files but share repository metadata. They do
not isolate ports, credentials, databases, cloud services, native browsers or
shared documents. See the [official worktree guide](https://learn.chatgpt.com/docs/environments/git-worktrees).

Record the owner of each branch, server, shared file, account state and QA target.
Freeze the served build during QA. Do not rebuild or stop another worker's
server unannounced. Give overlapping coordination records one editor, or supply
a patch for the owner to apply (not for source where a project adopts a sole
writer; there others deliver findings or specs). Integrate reviewed changes
without dropping another worker's contribution.

Only one worker controls a native browser or device at a time. Agree on the
window/session and control handoff; capture initial settings, restore authorized
temporary changes and close only owned windows. Remove only verified test
state. Prefer purpose-built connectors or APIs where appropriate, and the
internal browser for ordinary browsing when available. Native browser/device
checks need the corresponding actual capability. A hidden window or controller
timeout is a tooling limit until a product failure is reproduced.

## One deliverable index across parallel projects

A project running several workstreams in parallel may adopt one private index
of deliverables rather than a status note per workstream. If it does, use the
[deliverable index template](../templates/DELIVERABLES.example.md). Each row has
an accountable owner, the evidence that supports its state, the next gate and a
reference to where restricted material lives. The index points to sensitive
files, messages and accounts; it never copies them into shared source. The index
is a pointer, not the status record: keep the canonical state in the project's
current status record and fix a stale row rather than adding a second narrative.

Whether or not an index is adopted, track three decisions separately; one does not imply another:

- **Preferred direction**: the human's visual or design choice among options.
- **Approved for launch**: the exact version may go live or be produced.
- **Approved to share**: the exact version may go to a named audience.

For a controlled visual review, compare options under the same framing, record
target-size fields and detail checks, and state what changed and what stayed
unchanged against the prior version. See the
[sanitized visual review example](../templates/VISUAL-REVIEW.example.md).

## Message approvals and quiet progress

By default, existing applicable authorization covers a send. Where a project
wants stricter control, it may adopt **per-message approval** in its overlay: show
the actual final draft as shown, the audience or destination, and the links and
attachments. Approval covers only that material version; any change reopens
review. Record a dispatch receipt, or that the human sent it. An item the human
sent is never resent by an agent, and a failed or uncertain send is never
resent automatically: inspect the destination first, then ask.

A project may also adopt quiet progress reporting. If it does, routine steps and
unchanged status are not reported; surface a material milestone or blocker with
its limits (what is verified, what is not) and the next action, owner and
decision needed. Silence is not a completion claim. Without that adoption,
follow the project's existing reporting practice.

## Durable records and safe cleanup

Choose one ownership directory and one current status/release record per project.
Keep detailed task evidence in dated folders. Preserve old specs/plans/receipts
or append explicit corrections; an old pass does not cover new code. Where a
project uses complete-code plans, merged code is authoritative and the plan
becomes dated history.

Commit sanitized instructions, reviewed changes and portable evidence to the
appropriate work repository. Keep private source messages, customer data,
authenticated URLs, credentials and machine/session files in their approved
restricted system. Reference provenance rather than copying it into Git.
Retain important artifact versions, hashes and inspected output.

Before archiving a chat or removing a worktree, preserve deliverables, unmerged
work, necessary ignored artifacts, decisions and remaining tasks. Verify the
continuing owner's handoff. Archiving is not task completion, and moving a
summary does not merge chat histories.
