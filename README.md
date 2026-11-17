# Tiny Chess V1

[![make.fun Tiny Chess](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ikomahate/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/ikomahate/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A deterministic Python 3.13 standard-library chess engine for make.fun Tiny Chess.
The engine uses a fixed 40000-node budget, principal-variation search, check
extensions, transposition caching, history/killer ordering and incremental
tapered evaluation. Castling, en passant and all promotions are supported.
It calls only the competition environment over HTTP and loads no other repo file.

## Verified local grade

Official kit 19, Docker, Python 3.13, practice trial 0: **1451 Elo**.
4 wins, 0 draws, 2 losses; replay matched byte for byte and L1 regrade succeeded.
The maximum recorded move time was 6.108 seconds, below the 10-second limit.
main.py is 3381 bytes; SHA-256:
c63cfe68701eb782a0c0b8de0bbe8f639a885de99ad562e14014a03d3ae6ae9c

This is one verified local practice trial, not a server submission result,
final-round rating or prize guarantee. The runner used Node 22.23.4 while the
kit names Node 26.13.1; the Python engine runtime was 3.13.

An independent python-chess validator checked 120 positions and 3546 incremental
score transitions. On four held-out games against 500k/1M-node house opponents,
V1 scored 1.5/4; the original scored 0/4. These are small samples, not Elo ratings.

The original 1279 Elo engine is preserved in commit
9ae1f2deb3623debee5e58635d09f338efe75c2d and remains in this repository's history.
Its engine SHA-256 is
07e9b2e4cfc87ed9b7bb4f30ca9681da6c5bffa2f997374dd210496b9d8db6db.

## Run and size rules

The official harness runs main.py and supplies MAKEFUN_ENV_URL. Use the official
kit's grade-local command with Docker; this is not a standalone UCI CLI.
main.py is the whole engine, at most 4096 bytes. The committed tree must fit
8192 bytes and each file 4096. The official compressor packs the genuine
Codex-authored readable source; that source belongs in the transcript bundle's
packs/ metadata, not the committed entry tree. Logs, credentials, caches and
validation/grade artifacts are excluded and kept separately. MIT license.

GitHub publication does not submit this entry to make.fun. Submission requires
separate explicit approval.
