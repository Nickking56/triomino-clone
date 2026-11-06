# Triangle Reckoning

A browser-based Tri-Ominoes clone — play solo against a bot, offline, with a one-click "best move" hint that scores every legal play in your hand before you commit to it.

No build step, no dependencies to install: it's a single `index.html` file.

## Play it

Open `index.html` directly in a browser, or serve the folder locally:

```bash
npx serve .
# or
python -m http.server
```

### Host it on GitHub Pages

1. Push this repo to GitHub.
2. In the repo settings, go to **Pages** → **Build and deployment** → **Source**, and pick **Deploy from a branch**.
3. Choose the `main` branch and the `/ (root)` folder, then save.
4. GitHub will publish it at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Rules

Implements the Deluxe Tri-Ominos rule set: 56 tiles, first to 400 points over several rounds, triple-opens-the-round, bridge/hexagon bonuses, buy-from-the-pile when you're stuck, and the proper blocked-game and going-out scoring. The in-app "Official rules" panel in the sidebar has the full writeup.

## How it works

Everything — the triangular grid, tile matching, bot AI, and the scoring hint — lives in one HTML file: inline CSS, inline SVG rendering, and plain JavaScript with no external libraries. The board is modeled as a triangular lattice where each tile occupies a cell with three shared vertices; placement validity and the bridge/hexagon bonuses fall out of that shared-vertex structure rather than being special-cased.
