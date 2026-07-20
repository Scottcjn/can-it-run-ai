# Contributing

## Submitting a run

Open an issue with the [submission template](../../issues/new?template=submission.yml). That is the whole process from your side.

## Review process

1. A maintainer checks what can be checked: sha256 checksums against the linked binary and model, raw logs for internal consistency (timestamps, token counts vs. reported speed), and the video if one is provided.
2. Entries that check out are added to [LEADERBOARD.md](LEADERBOARD.md) as **Verified**. Entries with published claims but incomplete evidence are added as **Pending** with a note saying exactly what is missing.
3. If someone challenges an entry, it is marked **Disputed** while the maintainer re-checks. Corrections are normal here; entries get fixed, not deleted, unless the claim was misrepresented (for example, emulation presented as real hardware).

## Failed attempts

Failed attempts are welcome and get their own section on the leaderboard. Negative results are data: knowing that a port dies at link time on some platform, or that a model does not fit, saves the next person a weekend. Submit them with the same template and put the failure details in the limitations field.

## Emulation

Emulated runs are fine as long as they are labeled. Several verified entries here are emulated and say so. The one thing that gets an entry pulled is presenting an emulated run as real hardware.
