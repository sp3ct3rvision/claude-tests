# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Single-file browser games and web experiments. Currently: a Tic-Tac-Toe game in `tictactoe.html`.

## Running the project

Open any `.html` file directly in a browser — no build step, no server, no dependencies. All CSS and JS are inline in each HTML file.

## Architecture

Each project is a self-contained `.html` file with three inline sections:

- `<style>` — all styling, dark theme (`#1a1a2e` background, `#e94560` accent)
- `<body>` — semantic HTML structure
- `<script>` — vanilla JS, no frameworks or external libraries

**Tic-Tac-Toe state model:** `board` is a flat 9-element array indexed `0–8` (row-major). `WINS` is a hardcoded array of winning index triples. Game state lives in module-level variables (`board`, `current`, `gameOver`, `scores`). DOM cells are selected once at load and referenced via `cells[i]`.

## Git workflow

All changes must be committed and pushed to `https://github.com/sp3ct3rvision/claude-tests` regularly so work is never lost and can always be reverted.

- Commit and push after every meaningful unit of work (new feature, bug fix, notable edit)
- Never leave a working session without pushing — the GitHub copy is the source of truth
- Use concise imperative commit messages (e.g. `Add win animation`, `Fix draw detection`)
- Always include the co-author footer:
  ```
  Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
  ```
