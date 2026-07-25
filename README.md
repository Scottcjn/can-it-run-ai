# Can It Run AI?

A community leaderboard for running real AI inference, or verified compute, on vintage and exotic silicon. Prove it or it didn't happen.

**Live leaderboard: [scottcjn.github.io/can-it-run-ai](https://scottcjn.github.io/can-it-run-ai/)** — includes the Weird Hardware Hall of Fame (unclaimed firsts: Dreamcast, TI-83, PlayStation 1, C64, Transputer, and more).

Museum page: [elyanlabs.ai/can-it-run-ai.html](https://elyanlabs.ai/can-it-run-ai.html)

The site is driven by [`docs/leaderboard.json`](docs/leaderboard.json) — verified entries are added there and to [LEADERBOARD.md](LEADERBOARD.md) together.

## What this is

People keep asking whether old machines can do anything useful with modern AI. The honest answer is: some of them can, if you are willing to shrink the model, port the code, and measure what actually happens. This repo tracks who has done that, on what hardware, at what speed, with proof.

Entries range from a 819K-parameter transformer generating text on a Nintendo 64 to llama.cpp running on PowerPC Macs under Tiger and Leopard. Verified non-inference compute (for example, a vintage machine doing real attested work) counts too, as long as it is labeled for what it is.

Current standings: [LEADERBOARD.md](LEADERBOARD.md)

## The rules

1. **Real hardware or honestly labeled emulation.** Native execution on the actual machine is the gold standard. Emulated runs are welcome and useful, but they must be clearly labeled as emulated. An emulated run presented as real hardware gets the entry pulled.
2. **Proof required.** One of:
   - an uncut boot-to-output video, or
   - raw logs plus sha256 checksums of the binary and the model file.
   Both is better.
3. **Honest limitations section required.** Every submission must state what the demo does not show: tiny model, cherry-picked prompt, emulator quirks, thermal throttling, whatever applies. Entries without one are marked pending until it is added.
4. **Corrections welcome.** If you think an entry overstates its claim, open an issue. Disputed entries get marked as disputed while we sort it out. Being corrected is not a penalty; overstating and leaving it there is.
5. **Failed attempts count.** Negative results are data. If you tried and it did not work, submit anyway. Failed attempts get their own section on the leaderboard.

## How to submit

Open an issue using the [submission template](../../issues/new?template=submission.yml). It asks for machine, year, CPU, RAM, what you ran, speed, proof links, checksums, and your honest-limitations section.

A maintainer will verify what can be verified (checksums, logs, video) and add the entry to the leaderboard as verified or pending. See [CONTRIBUTING.md](CONTRIBUTING.md) for the review process.

## Verification

The verification methodology here borrows from RustChain's hardware fingerprinting work on distinguishing real vintage silicon from emulation ([rustchain.org/proof-of-antiquity.html](https://rustchain.org/proof-of-antiquity.html)): timing behavior, cache characteristics, and honest self-reporting of emulated environments.

## License

AGPL-3.0. Copyright (C) 2026 Elyan Labs LLC. See [LICENSE](LICENSE).
