# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/rhafarnulis/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/rhafarnulis/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine in a single 4,026-byte main.py: alpha-beta search with PVS, quiescence, transposition table and a fixed node budget (deterministic, no clock). Local practice Elo ~1,365 against the house gauntlet (trials 1,451 / 1,364 / 1,279), above the sunfish baseline (~1,325).

## How it plays

Iterative deepening (depth 1–6) with a fixed node budget per depth, killer moves, history heuristic, null-move pruning and a PST + pawn-structure evaluation. It talks to the game env over HTTP (`MAKEFUN_ENV_URL`) and plays the move the search picks.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8000 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=2s4v23h1&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
