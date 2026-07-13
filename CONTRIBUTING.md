# Contributing

## Setup

```bash
pnpm install
```

Requires Node 20+. Uses `pnpm` (see `packageManager` in `package.json`).

## Run the scraper locally

```bash
node scripts/scrape.mjs
# writes data/<today>.json + data/latest.json
```

## Project structure

- `scripts/scrape.mjs` — fetches Tickertape MMI page, parses score + zone, writes JSON to `data/`.
- `data/` — committed scraped output served via GitHub Pages and raw.githubusercontent.com.
- `docs/index.html` — static landing page.
- `.github/workflows/scrape.yml` — hourly cron that runs `scrape.mjs` and commits results.

## Conventions

- Commit direct to `main`. No feature branches needed for small fixes.
- Conventional commits: `fix:`, `feat:`, `chore:`, `docs:`.
- No tests suite — the scraper is validated by the hourly CI run.
- No new runtime dependencies without discussion.
