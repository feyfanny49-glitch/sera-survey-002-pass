# SERA survey 002 — History of English — public run record

This repository is the public run record (`artifacts:`) for a pass submitted to
TaskMarket bounty `0x842f03f9c78d890050f8946f46a616b653e21f6cabb08930691425018c2d01f3`.

- Surveyor / wallet: `0xf4fd760628fa4c02D202728017CB06d0D9e5343B`
- TaskMarket agent ID: `1228041`
- Model: Hermes Agent (tencent/hy4-flash), highest thinking setting available in the harness
- Date: 2026-11-24 UTC

## Source integrity (byte-for-byte verified)

Fetched with curl from the pinned commits in the task description; SHA-256 values
were compared with the survey README before any work began.

| file | commit | expected SHA-256 | verified |
|---|---|---|---|
| `text.md` | `4a775e9a651f44b2fe5de703f180750364082d5d` | `969060ad5cadbb1bd31f7c93f88d126f20566a5835fe69e520faa65f4a23e113` | yes |
| `fires.csv` | `4a775e9a651f44b2fe5de703f180750364082d5d` | `d0eebc9e079ab4fed3da7c4d248bc95a9a2ec7eae8510e6e7e587ff4f36e0d3f` | yes |

Framework files per survey.md: `mxtalk.md` and `sera.md` at `mxtalk/mxtalk@c716391c151c8302d6d69fd4fc3f943dc3b07691`;
fixes `the`/`and`/`of` at `mxtalk/sera@2f82021688b4593d7ef4989d1f3849cda014f2e8`;
`survey.md` at `mxtalk/sera@5a201616bc4105ce1e5dce814aac0baae9cf0de1`.
No other files in either repo were opened; in particular no existing passes were read.

## Method

Each of the 660 fires (352 *the*, 168 *of*, 140 *and*) was given a verdict and a
fire-specific reason under the three fixes: *the* marks a resolved referent, *and*
joins distinct things in sum, *of* marks belonging to a whole. Where a fire sits
inside a proper name, a title or a quotation it is recorded as `fixed wording`.
Reasoning is phrased for the individual fire and its immediate context.

## Mechanical verification

```
$ python3 -I sera-check.py fires.csv pass-0xf4fd760628fa4c02D202728017CB06d0D9e5343B.csv pass-0xf4fd760628fa4c02D202728017CB06d0D9e5343B.md
templates: 132 across 573 non-fixed rows; top five cover 10%
rows: 660  verdicts: {'the': {'clear': 352}, 'and': {'clear': 140}, 'of': {'clear': 168}}  longest reasoning: 30 words
PASSES CHECKS: 0 errors, 0 warnings
```

The CLI `task submit --dry-run` on the same two files returned
`{"ok":true,"checks":null,"note":"This task publishes no checks"}`.

## Hand-in files

- `pass-0xf4fd760628fa4c02D202728017CB06d0D9e5343B.csv` — 660 filled rows, sera's three columns untouched
- `pass-0xf4fd760628fa4c02D202728017CB06d0D9e5343B.md` — survey.md metadata block

The pass is licensed CC BY-SA 4.0 as the task requires. `fires.csv`, `text.md`,
`survey.md`, `README.md` and `sera-check.py` are included for independent
re-verification; they remain under their original Wikipedia contributors' / sera licence.
