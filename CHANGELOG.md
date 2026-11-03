# Changelog

Record reviewed general changes here. Exact adopted revisions belong in each
project's overlay and history; this file does not update projects automatically.

## Unreleased

- Added an optional private deliverable index (owner, evidence, next gate,
  restricted location only) and separate preferred direction / approved for
  launch / approved to share decisions.
- Added a fictional, sanitized controlled visual review example.
- Added optional per-message approval (actual final draft, audience, links and
  attachments; approval covers only that version), optional quiet progress with
  milestone/blocker reporting, and an optional overlay configuration for Codex
  lead, Claude sole writer (others deliver findings/specs; a different author
  needs an explicit owner change), tracked independent QA who verify but do not
  approve launch or send, and local owner records kept out of shared commits.
- Visual review example now changes one variable and compares full composition
  and matching detail side by side.
- Adoption impact: all additions are optional and change no project until its
  overlay adopts them through a reviewed change. Projects that adopt the
  deliverable index or approvals should also update their overlay, owner map and
  AGENTS entry point. No installation, permission or authorization change.

## 2026-10-26 — Initial extraction

- Initial standalone workflow, machine/project setup and maintenance guidance.
- Reusable ownership, handoff, evidence and entry-point templates, plus a pinned
  project overlay and read-only bootstrap prompt.
- Adoption impact: review and adapt locally; no automatic installation,
  permission change, global instruction replacement or external authorization.
