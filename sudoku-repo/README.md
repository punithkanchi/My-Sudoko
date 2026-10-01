# Sudoku

A self-contained, single-file Sudoku game — built as a light-mode web app inspired by the layout of [sudoku.com](https://sudoku.com) (difficulty tabs, mistakes/timer panel, number pad, rules section), written entirely from scratch: original code, original puzzle generator, original rule write-ups.

**Live demo (after you deploy):** `https://<your-username>.github.io/<your-repo-name>/`

## Features
- Real puzzle generator (backtracking + uniqueness check) — a fresh, solvable puzzle every game, not a fixed set
- 6 difficulty levels: Easy, Medium, Hard, Expert, Master, Extreme
- Mistake tracking (3 allowed before auto-restart), hints, undo, pencil notes
- Pause/resume — blurs the board and stops the timer
- A "Rules" tab with an expandable card for each core solving technique (Last Free Cell, Last Remaining Cell, Last Possible Number, Notes, Obvious Singles, Obvious Pairs)
- Zero dependencies — one HTML file, inline CSS/JS, Google Fonts (Baloo 2 + Nunito) loaded via CDN

## Run it locally
Just open `index.html` in any browser. No build step, no server, no npm install.

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
open index.html   # or just double-click the file
```

## Deploy free with GitHub Pages
1. Push this repo to GitHub (see below if you haven't yet).
2. On GitHub, go to your repo → **Settings** → **Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`.
4. Set **Branch** to `main` (or `master`) and folder to `/ (root)`. Save.
5. Wait a minute, then your game will be live at:
   `https://<your-username>.github.io/<your-repo-name>/`

## Pushing this to your GitHub account for the first time
```bash
cd sudoku-repo
git init
git add .
git commit -m "Initial commit: Sudoku game"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git push -u origin main
```

## File structure
```
sudoku-repo/
├── index.html   # the entire game — markup, styles, and logic
└── README.md
```

## Customizing
- **Difficulty clue counts** — edit the `diffClues` object near the top of the `<script>` block.
- **Colors/fonts** — CSS custom properties are defined at the top of the `<style>` block under `:root`.
- **Rules content** — edit the `ruleTopics` array in the script to change wording or add topics.
