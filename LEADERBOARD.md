# Leaderboard

Entries are listed with their proof. Status meanings:

- **Verified**: proof checked by a maintainer (repo, logs, screenshots, video, or third-party coverage).
- **Pending**: claim published, but some evidence is still being captured or confirmed.

Speeds are as measured on the specific machine and model listed. A 819K-parameter model on an N64 and TinyLlama on a POWER8 are not comparable numbers; read the "What it runs" column.

## Inference

| Machine | Year | CPU | RAM | What it runs | Speed | Proof links | Status |
|---------|------|-----|-----|--------------|-------|-------------|--------|
| Nintendo 64 | 1996 | MIPS R4300i (93 MHz) | 4 MB | Legend of Elya, 819K-param nano-GPT transformer, float32 | ~60 tok/s (61.8 tok/s in captured run) | [Repo + ROM](https://github.com/Scottcjn/legend-of-elya-n64) · [Video: first coherent output](https://bottube.ai/watch/shFVLBT0kHY) · [Video: full demo](https://bottube.ai/watch/7GL90ftLqvh) · [DOI 10.5281/zenodo.21435983](https://doi.org/10.5281/zenodo.21435983) · [HN thread](https://news.ycombinator.com/item?id=47105087) | Verified (emulator); real-hardware run via EverDrive 64 claimed in repo, video capture pending |
| Sun Cobalt Qube 3 | 1998 | AMD K6-2/450 | (stock unit) | Same 819K nano-GPT, ported to C89, built with gcc 2.95 on the stock 2001 Cobalt Linux image | ~12 tok/s (64 tokens / 5.30 s CPU) | [Port docs](https://github.com/Scottcjn/legend-of-elya-n64/tree/main/cobalt-qube3) · [Terminal capture](https://raw.githubusercontent.com/Scottcjn/legend-of-elya-n64/main/cobalt-qube3/oracle_k6_run.png) | Verified (README + screenshot; no video yet) |
| PowerPC Macs (Power Mac G5 dual 2.0, iMac G5, PowerBook G4 1.67, Power Mac G4 dual 1.25) | 1999-2005 | PowerPC G4 / G5 | per machine | llama.cpp ported to Mac OS X Tiger and Leopard, TinyLlama | ~3-5 t/s on G5, ~1-2 t/s on G4 | [llama-cpp-tigerleopard](https://github.com/Scottcjn/llama-cpp-tigerleopard) · [Hackster.io coverage (Nick Bild)](https://www.hackster.io/news/the-powerpc-has-still-got-it-c4348bd7a88c) · [vec_perm paper, DOI 10.5281/zenodo.21282030](https://doi.org/10.5281/zenodo.21282030) | Verified (port + tested-hardware table + third-party press; no public screenshots or video yet) |
| IBM POWER8 S824 | 2014 | Dual 8-core POWER8, SMT8 | 512 GB | llama.cpp with PSE / RAM Coffers optimizations, TinyLlama 1.1B Q4 | 147.5 t/s prompt (pp128), 18.9 t/s generation (tg32); 8.8x stock llama.cpp | [ram-coffers](https://github.com/Scottcjn/ram-coffers) · [Dated evidence still](https://raw.githubusercontent.com/Scottcjn/ram-coffers/main/youtube-evidence-dec17-2025.png) · [PSE paper, DOI 10.5281/zenodo.18623922](https://doi.org/10.5281/zenodo.18623922) · [RAM Coffers paper, DOI 10.5281/zenodo.18717767](https://doi.org/10.5281/zenodo.18717767) · [Benchmark charts](https://github.com/Scottcjn/Rustchain/tree/main/benchmarks/pse/sample_results/charts) | Verified claims published; reproducible raw logs pending |

## Verified compute (not inference)

Real work on vintage platforms that is not LLM inference. Labeled as such on purpose.

| Machine | Year | CPU | RAM | What it runs | Speed | Proof links | Status |
|---------|------|-----|-----|--------------|-------|-------------|--------|
| Amiga (classic AmigaOS, m68k) | 1985-1994 platform | Motorola 68k (emulated via FS-UAE) | per config | RustChain miner + SDK + tools + micro-JVM + bootable AROS distro, live-attesting to the production network. Self-detects UAE and reports emulation honestly. No LLM inference on this platform yet. | n/a (attestation, not inference) | [rustchain-amiga](https://github.com/Scottcjn/rustchain-amiga) · [Proof of Antiquity paper, DOI 10.5281/zenodo.18623592](https://doi.org/10.5281/zenodo.18623592) | Verified (emulated, honestly labeled; no real-hardware run documented) |
| Sun Cobalt Qube 3 | 1998 | AMD K6-2/450 | (stock unit) | rustchain-vintage-x86: single-file C89 RustChain miner for 486/Pentium/K6 on kernel 2.0/2.2, written for this Qube. RDTSC clock-drift fingerprint, honest hypervisor reporting. | n/a (attestation, not inference) | [rustchain-vintage-x86](https://github.com/Scottcjn/rustchain-vintage-x86) | Verified |

## Failed attempts

Negative results are data. Nothing here yet. Tried something and it did not work? [Submit it](../../issues/new?template=submission.yml).

| Machine | Year | CPU | What was attempted | Where it failed | Proof links |
|---------|------|-----|--------------------|-----------------|-------------|
| (none yet) | | | | | |
