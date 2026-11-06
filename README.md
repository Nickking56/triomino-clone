# Triangle Reckoning

**[▶ Play it now in your browser](https://nickking56.github.io/triomino-clone/)** —

## Features

- Full triangular-grid board, rendered live as tiles are placed
- A bot opponent for offline, single-player games
- "Show best move" — scans your whole hand and surfaces the highest-scoring legal play, including bridge and hexagon bonuses
- Light and dark themes
- Implements the Deluxe Tri-Ominos rule set: 56 tiles, first to 400 points over several rounds, triple-opens-the-round, bridge/hexagon bonuses, buying from the pile when stuck, and proper blocked-game / going-out scoring (see the "Official rules" panel in-app for the full writeup)

## Running it

Clone the repo and open `index.html` in a browser — that's it.

To serve it locally instead (useful if your browser blocks local file access for some features):

```bash
npx serve .
# or
python -m http.server
```

### Deploying your own copy

This is a static site, so it works as-is on GitHub Pages, Netlify, Vercel, or any static host. For GitHub Pages:

1. Fork or clone this repo to your own GitHub account.
2. In that repo's **Settings → Pages**, set **Source** to **Deploy from a branch**, pick the `main` branch and `/ (root)` folder, and save.
3. It'll be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## How it works

Everything — the triangular grid, tile matching, bot AI, and the scoring hint — lives in one HTML file: inline CSS, inline SVG rendering, and plain JavaScript with no external libraries. The board is modeled as a triangular lattice where each tile occupies a cell with three shared vertices; placement validity and the bridge/hexagon bonuses fall out of that shared-vertex structure rather than being special-cased.

## License

No license has been specified yet — all rights reserved by default. If you'd like to reuse this code, open an issue or reach out to the repo owner.
