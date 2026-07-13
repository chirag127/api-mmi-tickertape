# Security Policy

## Supported versions

Only the latest commit on `main` is supported.

## Scope

This repo scrapes a public webpage and serves static JSON. No user data, no secrets stored, no authentication. The scraper script (`scripts/scrape.mjs`) reads a public URL via HTTP and writes JSON files committed to the repo.

Relevant attack surfaces: GitHub Actions workflow injection, supply-chain issues in `cheerio` dependency, or a compromised scrape target poisoning the served data.

## Reporting a vulnerability

Use [GitHub Security Advisories](https://github.com/chirag127/mmi-tickertape/security/advisories/new) to report privately. Alternatively open a private issue or email chirag127 via the contact on [github.com/chirag127](https://github.com/chirag127).

Please include: what you found, reproduction steps, and potential impact. Expect a response within 7 days.
