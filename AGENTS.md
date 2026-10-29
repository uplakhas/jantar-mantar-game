# AGENTS.md

## Architecture
- Static site: everything (markup, styles, game logic) lives in `index.html`. No framework, bundler, or package.json.
- `netlify.toml` publishes the repo root.

## Structure inside index.html
- Screens are `.screen` divs toggled via `showScreen(id)`: login, home, profile, settings, game, gameover.
- State is stored in `localStorage` under `jm_currentUser` and `jm_allUsers`. A user is identified by name + country.
- Game engine: canvas `requestAnimationFrame` loop in `gameLoop()`; 3 lanes; level = floor(score/500)+1; speed scales with level.
- Music: hidden YouTube IFrame player, started in `startGame()` and paused in `endGame()`.

## Conventions
- Keep it a single-file, no-build site unless the owner asks otherwise.
- Theme colors are CSS variables in `:root` (neon pink on near-black; Orbitron + Poppins fonts).
- The leaderboard is per-browser; making it global would need Netlify Database plus a Netlify Function.
