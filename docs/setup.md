# Set up and adopt the workflow

This guide transfers a working method, not accounts, permissions or chat state.
Use company-approved software and work identities. No specific model or app
version is required; verify the destination project's actual capabilities.

## New machine

1. Install the approved Codex application, Git and the project's runtime/package
   manager through approved channels. Install Claude or service CLIs only when
   the assigned work needs them. Check versions against project setup files.
2. Clone the correct work repository and inspect its remote, branch, local
   changes, applicable instructions and worktree inventory. Open it as the
   intended project. Keep work and personal repositories/accounts separate.
3. Read existing root and directory instructions before proposing changes.
   Keep durable guidance short and link to procedures. Skills and repository
   guidance have different purposes. See [official customization guidance](https://learn.chatgpt.com/docs/customization/overview).
4. Select the least-privilege company-managed permissions supported by the
   task and installation. Read-only suits orientation; an approved
   `workspace-write` setup may suit local development. Automatic approval review,
   if available and allowed, handles eligible requests; it does not replace QA
   or authorize every external action. Do not disable restrictions to mimic
   another computer. See [approvals and security](https://learn.chatgpt.com/docs/agent-approvals-security).
5. Reconnect necessary work accounts through their supported sign-in flows.
   Verify the intended organization/project and scope with a harmless read.
   Never migrate authentication files, browser profiles, keychains, session
   databases, tokens or an entire personal configuration directory. Connector
   access needs separate review: shell network restrictions do not universally
   govern apps/MCP. Consult the [configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference).
6. Install only approved skills/plugins that the project needs and record their
   source/version. Do not automatically install dependencies or enroll in updates
   because a shared guide changed. Use the Workloop guidance below if applicable.

## Pin a reviewed revision in each project

1. Obtain an authorized local copy of this shared repository. The human/project
   owner chooses an exact commit for review; do not silently follow `main` or
   substitute the newest revision during bootstrap.
2. Review that revision against the project's current rules. Copy and adapt the
   [overlay template](../templates/PROJECT-OVERLAY.example.md), for example as
   `docs/agent-workflow.md`. Record the shared repository, full commit SHA,
   reviewer/date, local overrides and authoritative project record paths.
   Its revision placeholder must be replaced before adoption. Do not fabricate
   a revision.
3. Merge short [AGENTS](../templates/AGENTS.example.md) and
   [CLAUDE](../templates/CLAUDE.example.md) entry points into existing local
   files through a reviewed project change. Never overwrite established root,
   directory or global instructions. Record which shared conventions the
   project adopts or changes. Governing system/developer instructions and human
   authorization still apply; the shared guide cannot weaken them.
4. Keep the pinned documents available through a verified local copy or exact
   commit links. If inaccessible, report the gap rather than claiming they were
   read. Template copies are project-owned adaptations, not automatically
   synchronized files.
5. Paste the [bootstrap prompt](../templates/BOOTSTRAP-PROMPT.md). Its output is a
   read-only orientation and proposed adoption diff, not installation, account
   changes, permission changes or a release.

Finish orientation with the right repository, instruction sources, owner map,
checks, available capabilities and remaining dependencies. Do not send emails,
create orders or change production to demonstrate setup. This process does not
promise automatic migration of chats, memories, plugins, settings or artifacts.

## Optional Workloop dependency

Workloop is a separate custom/private tool, not bundled with this repository or
standard Codex. The core coordination workflow works without it. If a project
requires Workloop for bug fixes, that local requirement still applies; report a
missing approved installation before the run rather than bypassing it.

With authorized access, use the maintained private
[one-command setup](https://github.com/robertmyrsater/workloop/blob/main/docs/one-command-setup.md)
and [portable setup](https://github.com/robertmyrsater/workloop/blob/main/docs/portable-setup.md)
guides. The maintainer supplies a pinned per-machine command. Review its signed
release, exact instruction changes and feedback destination; this repository
copies no installer or command.

The one-command installer enrolls summary feedback. Do not send employer project
summaries to a personal feedback repository without work approval. Without that
approval, use a separately reviewed no-feedback portable setup, or use ordinary
Codex coordination without Workloop where the project permits it. Background
updates are a separate opt-in. Do not inherit personal feedback/update enrollment
or unrelated task/run folders.

## Reference freshness

The official platform links above and in the workflow were checked for the
source guide on 26 October 2026. They were reused during this extraction without
a fresh platform check. Recheck official guidance and company policy during
installation; UI labels and available capabilities can differ. The shared guide
is not a promise about synchronization or migration features.
