# Author Taxes, Plain English

A beginner manual for self-employed authors and small-business owners whose
income lands on **Schedule C** — royalties from books, freelance income,
reselling, side businesses, and the honest, slightly messy reality of keeping
records without panicking.

Written by [Dylan Asdale](https://dylanasdale.github.io) / **Asdale Dynamics, LLC** —
a registered nurse turned AI author who explains things "like a friend would":
plain English, step by step, never condescending.

> **This is education, not tax advice.** Every person's situation is different,
> tax rules change every year, and only a qualified tax professional (CPA, EA,
> or tax attorney) can tell you what applies to *you*. Every chapter here ends
> by pointing you back to one. Use this to understand the vocabulary and walk
> in feeling prepared — not to file alone.

---

## What's inside

| Chapter | What it covers |
|---|---|
| [00 — Start Here](docs/00-start-here.md) | Who this is for, how the pieces fit, "am I self-employed?" |
| [01 — Schedule C in Plain English](docs/01-schedule-c-plain-english.md) | What the form actually is, line by friendly line |
| [02 — Tracking Royalties](docs/02-tracking-royalties.md) | KDP, IngramSpark, audiobooks, ad sales — where money comes from and how to log it |
| [03 — Deductible Expenses](docs/03-deductible-expenses.md) | What you can (and can't) subtract, in normal human words |
| [04 — Quarterly Estimates](docs/04-quarterly-estimates.md) | Paying-as-you-go when no employer is withholding for you |
| [05 — Receipts Without Panic](docs/05-receipts-without-panic.md) | ADHD-friendly, low-energy record keeping that actually lasts |
| [06 — When to Call a Pro](docs/06-when-to-call-a-pro.md) | Triggers, questions to ask, and what to bring |

**Printable companion:** a one-page expense checklist and a royalty log you can
keep on your desk — see [`site/printable-expense-checklist.html`](site/printable-expense-checklist.html).

## Is this the guide you need?

Dylan writes three related guides. They are siblings, not twins:

| Guide | For you if... |
|---|---|
| **This guide** | You have *Schedule C* income: royalties, freelance, an LLC's business activity, reselling, a side hustle. You are your own business. |
| `quarterly-taxes-calm-guide` | You have *W-2* income and just want to understand withholding, adjustments, and safe estimates on the employee side. |
| `llc-first-year-handbook` | You're forming or running an LLC's **operations** — registered agent, EIN, bank account, operating agreement, bookkeeping setup. |

- A **dependent contractor/LLC member** choosing an employee-retention model? Read this one plus the LLC handbook.
- **W-2 pay stub** confusing you about estimated payments? That's the quarterly guide.
- **History records or paper trail** missing? This one (royalties + receipts) is your home base.

## Running the site

No build step. It's plain HTML, meant to be read locally or printed.

```bash
# option 1: open directly
open site/index.html          # or double-click it

# option 2: serve locally (nicer URLs)
cd site && python3 -m http.server 8000
# then visit http://localhost:8000
```

Inside the checklist (`site/printable-expense-checklist.html`), hit **Ctrl+P
/ Cmd+P** — it's styled to print cleanly on one sheet, front and back.

## Repository layout

```
docs/         the manual (markdown, one chapter per situation)
site/         static HTML: landing page + printable checklist
LICENSE       MIT — Copyright (c) 2026 Asdale Dynamics, LLC
STATUS.md     what's built, how it was verified, known gaps
```

## Credits & license

Maintained by **Asdale Dynamics, LLC** (Dylan Asdale), Indiana. Education
project; nothing here is legal, tax, or medical advice. MIT licensed — see
[LICENSE](LICENSE). IRS.gov is always authoritative for the current numbers.

*Be kind to future-you. Keep the receipts.*
