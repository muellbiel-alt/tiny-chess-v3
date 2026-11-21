# tiny-chess-v3

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/muellbiel-alt/tiny-chess-v3/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/muellbiel-alt/tiny-chess-v3/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python 3.13 (standard library only) for make.fun's tiny-chess-01: principal-variation search with quiescence, a 65,536-entry transposition table, MVV-LVA plus killer/history move ordering, late-move reductions, null-move pruning, and an endgame king mop-up. It plays the house gauntlet through the env at MAKEFUN_ENV_URL, one move at a time, under a fixed node budget — no clock, no randomness, so every trial replays byte for byte.

## Run it

```sh
python3 -P -s main.py
```

`main.py` is the whole engine, packed from `engine_src.py` with `makefun compress`. It reads the position from the env (`MAKEFUN_ENV_URL`), searches, and posts its move back.

---

<sub>Entered on [make.fun](https://make.fun/?ref=56xpzyp1&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
