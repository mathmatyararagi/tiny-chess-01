# tiny-chess-01 entry

A chess engine in at most 4,096 bytes of Python (main.py), written for the
make.fun bounty "Build the strongest chess engine in 4 KB of Python".

main.py is the whole engine: it talks to the env at MAKEFUN_ENV_URL
(POST /game, POST /move) and plays every game of the gauntlet. The file is a
compressed payload (lzma + base85) with its unpacker, as the bounty rules
allow; the readable source was developed and tested locally against the
kit's practice trials.

Engine sketch: negamax alpha-beta with iterative deepening under a fixed
node budget (deterministic, no clock), quiescence over captures, promotions
and check replies, a transposition table, killer-move ordering, and an
evaluation of material, piece-square terms, bishop pair, pawn structure
(doubled and passed pawns), rook files and king pawn shield.

License: MIT (see LICENSE).
