[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/besan11/tiny-chess-v5/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/besan11/tiny-chess-v5/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess-v5

A chess engine in 4 KB of Python, built for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty, $500 in USDC.

Engine-only: no opening book. A 0x88 board with tapered piece-square tables computed at import, principal-variation search with null-move pruning and late-move reductions, quiescence search with delta pruning, a transposition table, killer moves, and repetition detection against the game history and the search path. It searches to a fixed budget of 100,000 nodes per move, never a clock, so every trial replays move for move.

Local practice (simulated house gauntlet): trial-0 Elo 1279 (run twice, identical moves), trial-1 1191, trial-2 1364, final-like A 1253, final-like B 1173.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 -P -s main.py
```

The engine talks to the trial environment alone: `POST /game` to start, `POST /move` to play. It calls no model and no other service.

---

<sub>Entered on [make.fun](https://make.fun/?ref=jpgk45b3&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards · Referral: https://make.fun/r/jpgk45b3</sub>
