# Verification receipt — example

- Checked at / tester / independent reviewer: `[timestamp with timezone; roles]`
- Original outcome and acceptance: `[source]`
- Project overlay / reviewed shared revision: `[path and full SHA]`
- Repository/base/head/tree: `[exact versions]`
- Artifact hashes / dirty-source manifest / served build: `[identities]`
- Environment, configuration and fixtures: `[non-secret details]`
- Browser/device/OS/tool versions: `[relevant verified facts]`
- Authority and exclusions: `[permitted actions; held actions]`

| Case | Evidence kind | Steps and expected result | Actual result | Status | Receipt |
| --- | --- | --- | --- | --- | --- |
| `[case]` | `[local / emulated / native / provider / human report]` | `[steps]` | `[observation]` | `[pass/fail/blocked/not-run]` | `[path/link]` |

For bug fixes retain baseline failures, positive controls, frozen check hashes,
candidate diff and review disposition. Explain test-contract revisions; do not
silently replace a failed baseline or weaken an assertion. Record commands,
exit results, counts and skips without claiming skipped tests passed.

## Integration and release

- Final reviewed source compared with tested source: `[result/differences]`
- Concurrent upstream work preserved: `[comparison]`
- Required fresh integrated checks: `[results]`
- Independent review disposition: `[exact reviewed version/findings]`
- Publication/merge/deploy/send authority: `[specific authorization or held]`
- PR / merged tree / deployment or delivery / live outcome: `[each verified separately]`
- Original intended outcome achieved: `[inspection, remaining gap or limitation]`

## Limits and cleanup

`[Untested cases; tooling failures versus reproduced defects; approved exceptions;
remaining dependency with execution owner and next action.]`

`[Initial settings; temporary state; restoration/removal verification; owned
windows/servers; retained evidence location; incomplete cleanup.]`

Sanitize for the destination. Keep secrets, raw customer records, signed tokens,
private messages and authenticated URLs in approved restricted systems. Reference
provenance without copying it into this receipt.
