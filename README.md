# Tiny Chess: official-packed candidate

[![make.fun Tiny Chess](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ikomahate/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/ikomahate/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01)

Separate local packaging candidate for the make.fun Tiny Chess bounty.
Python 3.13, standard library only, deterministic fixed-node search and the
competition HTTP environment protocol. No model calls or external engine data.

This main.py was produced by the official makefun compress command from the
real Codex-authored engine-source.py. Its decompressed Python payload is
byte-for-byte identical to the proven engine's payload. Packaging changes the
entrypoint bytes; **this candidate has not run an official Elo match**.
Do not assign the proven engine's Elo score to this candidate or replace that
engine before a new official grade is authorized and confirms the result.

The separate proven engine is 3501 bytes, SHA-256
4fab95d64bd85e4c7df2b7031b93ebce10edd9cf0a147f51fa3ff4d668201773.
Its saved Docker/Python 3.13 local grade is 1279 Elo, 3 wins and 3 losses,
with matching replay and successful L1 regrade.

The harness supplies MAKEFUN_ENV_URL and runs main.py. Use the official kit
for evaluation; this file is not a standalone UCI command-line interface.

Planned GitHub target: ikomahate/makefun-tiny-chess. Not published or submitted;
the badge paths reserve that planned name only. GitHub About must link the
bounty and include the makefun topic before any future publication/submission.

The readable source is ignored by Git and belongs in the transcript bundle's
packs/ metadata, not the size-limited snapshot. Keep logs, reports and generated
bytecode out of the entry. Limits: 4096 bytes/file, 8192 bytes total. MIT license.
