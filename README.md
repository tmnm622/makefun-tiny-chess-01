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

---

<sub>Entered on [make.fun](https://make.fun/?ref=4ndxv2n7&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
