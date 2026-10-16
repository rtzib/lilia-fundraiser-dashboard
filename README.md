# Lilia's BBQ Fundraiser - Orders Dashboard

Live dashboard for Grandma Lilia's BBQ fundraiser (Sat, Oct 17, 2026, 6 PM, Suku'uno'ob).

- **Live page:** https://rtzib.github.io/lilia-fundraiser-dashboard/
- **Search engines:** `index.html` has a noindex tag so Google doesn't list it. Anyone with the link can still open it.
- **Data:** read straight from the order Google Sheet every 30 seconds. Nothing is stored here.
- **The sheet must be shared as "Anyone with the link: Viewer".** Add the people who take orders as editors by email.

## What's in here

| File | What it is |
|---|---|
| `index.html` | The whole dashboard (one file, no install). |
| `manifest.webmanifest`, `icons/` | App name and icon, so it can be added to a phone's home screen. |

## Updating

The numbers update on their own from the sheet. Only push a new commit when the dashboard itself changes.

## Settings (top of the script in `index.html`)

- `SHEET_URL` - the order sheet.
- `PRICES` - plate prices (Chicken 10, Pork 12, Italian Sausage 8).
- `EXTRA_PRICES` - extra pieces (tortilla 1, sausage 3; pork/chicken pieces not set, use a `$` price in the note for combos).
- `REFRESH_SECONDS` - how often it re-reads the sheet (30).

## Writing notes in the sheet

- Extras: `+1 tortilla`, `+2 sausage`, `+1 pork` (total for the order). Add `each` for per plate.
- Combos: `combo: +1 pork, +1 sausage $18`.
- A `$` amount in the note is that order's total price.
- Packing notes like `tortillas separate in foil` are fine.
