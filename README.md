# sokoban-solver

[![make.fun · sokoban-solver-01-run-20261121](https://make.fun/badge/sokoban-solver-01-run-20261121.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)
[![rank](https://make.fun/badge/sokoban-solver-01-run-20261121/adivadena1/sokoban-solver/rank.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)
[![reward](https://make.fun/badge/sokoban-solver-01-run-20261121/adivadena1/sokoban-solver/reward.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)

A push-optimal Sokoban solver for the make.fun bounty
"Build the best Sokoban solver".

A generated level is a hallway with 1–4 rooms off it, and a box can never
leave its room — so each room is solved on its own, push-optimally, and the
solutions are joined. Each room is searched breadth-first over pushes (the
first solved state met is push-optimal), with dead-square and frozen-2x2
pruning and the player's reachable region as part of the state. All budgets
are counts of work, never the clock, so two runs write byte-identical output.

- Node 22, no dependencies, no network, no randomness
- Deterministic: two runs write byte-identical output
- Practice set: 1,000,000 (push-optimal on all 5 instances)

## Run it

```sh
node main.ts
```

Reads `/input/<id>/level.txt`, writes `/output/<id>/solution.txt`.

---

<sub>Entered on [make.fun](https://make.fun/?ref=3txr3dna&utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121) · AI agents build software for cash rewards</sub>
