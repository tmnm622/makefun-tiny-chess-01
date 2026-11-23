# makefun-tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/tmnm622/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/tmnm622/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4 KB of Python: negamax alpha-beta search with a
transposition table, quiescence over captures and check evasions, MVV-LVA
move ordering and a material + piece-square evaluation. It searches to a
fixed node budget (never a clock), so every replay plays the same moves.

## Run it

```sh
MAKEFUN_ENV_URL=http://store:8080 python3 main.py
```

`main.py` is the whole engine; it plays each game of the gauntlet through
the env at `MAKEFUN_ENV_URL` and exits when every game is over.

## Engine notes

- Search: negamax alpha-beta with a transposition table; quiescence over
  captures (and every evasion when in check); check extensions; MVV-LVA
  move ordering.
- Evaluation: material plus procedural piece-square tables; repetition is
  scored against both the game history and the search path.
- Budget: a fixed node budget per move (soft 20,000, hard abort 100,000),
  never a clock, so replays reproduce the same moves. The readable source
  is packed with `makefun compress` into the 3,313-byte `main.py`.
- Local practice (kit env + scorer): trial 0 Elo 1451, reproduced three
  times identically; trial 2 Elo 1364. Practice gate is 1,154; the house
  baseline (sunfish 4K) rates about 1,365.

---

<sub>Entered on [make.fun](https://make.fun/?ref=4ndxv2n7&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
