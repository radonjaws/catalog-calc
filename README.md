# KTEQ-FM 91.3 — Clock & Library Calculator

A browser-based tool for designing broadcast clocks, building schedules, and calculating library size requirements.

## Features

- **Schedule grid** — 16 slots × 13 dayparts (editable), color-coded by category (G/S/B/C/R subcategories)
- **Clock library** — save any hour as a named clock, assign saved clocks to daypart columns, track usage counts
- **Specialty calculator** — separate SP1/SP2/SP3 pool grid with its own clock library
- **Track requirements** — spins/day → spins/week ÷ spins/track/week = total tracks needed + library hours
- **Persist** — all state saves to localStorage automatically; JSON export/import for sharing

## Deploying to GitHub Pages

1. Create a new repo (e.g. `kteq-calculator`) on GitHub
2. Drop `index.html` into the root
3. Go to **Settings → Pages → Source → Deploy from branch → main / root**
4. Your tool will be live at `https://<your-org>.github.io/kteq-calculator/`

## Local use

Just open `index.html` in any browser — no build step, no dependencies.

## Data format

JSON export includes:
- `clocks` — saved main clock library
- `grid` — current schedule grid (rows × cols of category codes)
- `scheduleColumns` — clock assignments per column
- `spinsPerTrack` — rotation depth per category
- `spClocks` — saved specialty clock library
- `spGrid` — specialty block grid
- `spScheduleColumns` — specialty clock assignments
- `spSpt` — specialty spins/track/week per pool

## Category codes

| Code | Category | Subcategories |
|------|----------|--------------|
| G1/G2/G3 | Gold | Heavy → Light |
| S1/S2/S3 | Silver | Heavy → Light |
| B1/B2/B3 | Bronze | Heavy → Light |
| C1/C2/C3 | Current | Heavy → Light |
| R1/R2/R3 | Recurrent | Heavy → Light |
| SP1/SP2/SP3 | Specialty | Heavy → Light |
