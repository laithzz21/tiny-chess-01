# Tiny Chess — a 4 KB Python chess engine

[![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/laithzz21/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/laithzz21/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01)

Entry for the make.fun bounty [Build the strongest chess engine in 4 KB of Python](https://make.fun/bounty/tiny-chess-01).

`main.py` (3,824 bytes) is the whole engine: a 0x88 board, negamax with
alpha-beta, iterative deepening under a fixed node budget (deterministic,
no clock, no randomness), quiescence search over captures, promotions and
check evasions, a transposition table, MVV-LVA + killer move ordering, and
an incremental material + piece-square evaluation with tapered king tables.
It plays the gauntlet through the env at `MAKEFUN_ENV_URL` and makes no
model calls.

The engine source is packed with LZMA + base85, which the rules allow: the
payload and its unpacker are inside the 4,096-byte cap.
