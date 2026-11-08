# STATUS — author-taxes-plain-english-guide

Last updated: 2026-11-08

## What was built

A beginner manual for author and small-business taxes (Schedule C side),
education-only, with a printable companion page:

- **`docs/`** — 7-chapter markdown manual:
  - `00-start-here.md` — who it's for, how it fits with the sibling guides
  - `01-schedule-c-plain-english.md` — what Schedule C is, form-shape walkthrough, SE tax preview
  - `02-tracking-royalties.md` — KDP/IngramSpark/audiobook/direct sales tracking, monthly ritual
  - `03-deductible-expenses.md` — ordinary/necessary/documented, author & reseller categories, COGS vs. expenses, "maybe" list pointing at a pro
  - `04-quarterly-estimates.md` — why pre-paying exists, set-aside habit, quarterly rhythm
  - `05-receipts-without-panic.md` — ADHD-friendly three-bucket record keeping, retention guidance
  - `06-when-to-call-a-pro.md` — tripwires, what to bring, questions to ask
- **`site/`** — static HTML, no build step:
  - `index.html` — landing page linking all chapters, sibling-guide table, local-run instructions
  - `printable-expense-checklist.html` — one-sheet printable expense checklist + royalty log with print CSS
- **`README.md`** — overview, chapter table, sibling-guide disambiguation, run instructions; credits Asdale Dynamics, LLC
- **`LICENSE`** — MIT, copyright line exactly: `Copyright (c) 2026 Asdale Dynamics, LLC`

Every chapter points to a tax professional; no specific IRS dollar amounts,
rates, or thresholds are stated (these change yearly — all defer to IRS.gov).

Deliberately distinct from `quarterly-taxes-calm-guide` (W-2 employee side)
and `llc-first-year-handbook` (LLC formation/operations) — disambiguation
tables exist in README.md, docs/00, and site/index.html.

## How to run it

```bash
# Site: open site/index.html directly, or serve:
cd site && python3 -m http.server 8000    # http://localhost:8000

# Printing: open site/printable-expense-checklist.html and Ctrl/Cmd+P
```

No dependencies, no build step, no network calls, no secrets.

## Verification results (2026-11-08)

- HTML well-formedness: both pages checked with Python `html.parser` —
  no mismatched or unclosed tags.
- Link check: all relative links in `site/index.html`,
  `site/printable-expense-checklist.html`, `docs/*.md`, and `README.md`
  resolve to existing files.
- Non-ASCII audit: only intentional characters (em dashes, curly quotes,
  `≠`, `☐`) remain; no stray/invalid characters.
- HTTP smoke test: `python3 -m http.server` served both pages with `200`.
- Print checklist verified to include print-specific CSS (@media print).
- Git: single repo, one initial commit `86b27f2`, committed as the existing
  local identity (`Dylan Asdale`), plain commit message, no co-author trailers,
  no remote configured, nothing pushed.

## Known gaps

- **Rates and dates intentionally omitted.** Standard mileage rates, SE tax
  rates, 1099 thresholds, simplified home-office rate, and quarterly due
  dates all live at IRS.gov and change yearly — the guide teaches where to
  look rather than numbers.
- Markdown is plain (no site generator); visitors to the GitHub Pages site
  render `.md` links via GitHub's renderer. A tiny build script could
  generate HTML from docs if that's ever wanted.
- No automated test suite — for a docs/static site, verification was
  script-based (parse + link + HTTP checks). Could be added later as a CI job.
- Sibling guides (`quarterly-taxes-calm-guide`, `llc-first-year-handbook`)
  are referenced but separate repos; links between them are by name only.
