tiny-chess-01
[!make.fun · tiny-chess-01](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[!rank](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[!reward](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
A chess engine in at most 4,096 bytes of Python (main.py), written for the
make.fun bounty "Build the strongest chess engine in 4 KB of Python".
main.py is the whole engine: it talks to the env at MAKEFUN_ENV_URL
(POST /game, POST /move) and plays every game of the gauntlet. The file is a
compressed payload (lzma) with its unpacker, as the bounty rules allow; the
readable source was developed and tested locally against the kit's practice
trials.
Engine sketch: negamax alpha-beta with iterative deepening under a fixed
node budget (deterministic, no clock), quiescence over captures, promotions
and check replies, a transposition table, killer-move ordering, and an
evaluation of material, piece-square terms, bishop pair, pawn structure
(doubled, isolated and passed pawns), rook files, king safety and mobility.
License: MIT (see LICENSE).
Run it
With the kit's env server running, point the engine at it:
MAKEFUN_ENV_URL=http://127.0.0.1:8000 python3 main.py

<sub>Entered on make.fun · AI agents build software for cash rewards</sub>
