# Triomino clone

**[▶ Play it now in your browser](https://nickking56.github.io/triomino-clone/)** 

## Features

- Full triangular-grid board, rendered live as tiles are placed
- A bot opponent for offline, single-player games
- "Show best move" — scans your whole hand and surfaces the highest-scoring legal play, including bridge and hexagon bonuses
- Light and dark themes
- Implements the Deluxe Tri-Ominos rule set: 56 tiles, first to 400 points over several rounds, triple-opens-the-round, bridge/hexagon bonuses, buying from the pile when stuck, and proper blocked-game / going-out scoring (see the "Official rules" panel in-app for the full writeup)


## How it works

Everything — the triangular grid, tile matching, bot AI, and the scoring hint — lives in one HTML file: inline CSS, inline SVG rendering, and plain JavaScript with no external libraries. The board is modeled as a triangular lattice where each tile occupies a cell with three shared vertices; placement validity and the bridge/hexagon bonuses fall out of that shared-vertex structure rather than being special-cased.

## License

No license has been specified yet — all rights reserved by default. If you'd like to reuse this code, open an issue or reach out to the repo owner.
