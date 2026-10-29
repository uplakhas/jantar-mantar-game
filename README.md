# Jantar Mantar — Endless Runner

A neon-styled, three-lane endless runner game for the browser. Players create a profile (name, age, country, language, avatar), dodge Indian street obstacles (autos, cows, chai stalls, barricades), collect ₹ coins, and climb a local top-5 leaderboard. An optional countdown timer mode and a looping phonk soundtrack (via the YouTube IFrame API) are included.

## Tech

- Plain HTML, CSS, and JavaScript in a single `index.html` — no build step
- HTML5 Canvas for the game loop
- `localStorage` for profiles, high scores, and the leaderboard (per browser)
- Hosted on Netlify as a static site

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
netlify dev --port 8889
```

## Possible next steps

- A global, cross-device leaderboard backed by Netlify Database
- Player accounts with Netlify Identity
