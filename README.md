# Nexus Chess

Play chess against [Nexus](https://markrozin.github.io/nexus-chess/), a chess
engine written from scratch in Rust, running entirely in your browser via
WebAssembly. Nothing is sent to a server.

The engine searches with alpha-beta, a transposition table, null-move pruning,
late move reductions and reverse futility pruning, and evaluates positions
with an NNUE (768->512x2->1) network. Strength is set by nodes per move.

This repository only hosts the page. `index.html` is built by `web/build.sh`
in the engine's own repository.

## Credits

The network was trained on the
[Lichess evaluation database](https://database.lichess.org/) (CC0), via the
deduplicated mirror
[mateuszgrzyb/lichess-stockfish-normalized](https://huggingface.co/datasets/mateuszgrzyb/lichess-stockfish-normalized)
(CC BY 4.0). Those evaluations come from Stockfish running in Lichess users'
browsers.
