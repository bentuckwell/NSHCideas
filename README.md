# NSHCS — Provider Page (V1)

A single-page interactive design for the **Provider detail page** of the National School of Healthcare Science (NSHCS) Trainee Management System. Built as a static HTML prototype to communicate layout, hierarchy, view/edit interactions and accordion behaviour.

## Live preview

`index.html` is fully self-contained — no build step, no dependencies. Open it directly in a browser, or serve the folder with any static host (e.g. GitHub Pages).

```bash
# locally
open index.html
# or
python3 -m http.server
```

## What's in here

- **Header** — NSHCS wordmark + NHS England logo, primary nav bar (Dashboard / Trainees / Provisions / Contacts / Locations), hero banner with back link, page title, status pills (Reaccredited, Closed case, Open case, Non engager, Watchlist), SharePoint folder link, section tabs and an Edit button.
- **Sidebar** — list of example providers (1–4); clicking one swaps the active provider title.
- **Provider name card** — locked-open accordion containing:
  - **Lead scientist** — contact details + "Show past contacts" expanding history.
  - **Annual monitoring contact** — same pattern as Lead scientist.
- **Hospital sites** — separate card listing 4 hospital site accordions, each containing:
  - **Head of department** — Name, Department, Email, Phone, Start/End date.
  - **Training officer** — same shape.
- **View / Edit mode** — clicking "Edit this page" in the hero:
  - Expands every accordion and hides chevrons.
  - Auto-opens every "Show past contacts" history list.
  - Replaces every value (text + dates) with form inputs.
  - Adds a "Remove contact" link beneath every contact, plus an "Add new contact" link at the top of every Head of department and Annual monitoring contact block (new entries scroll into view and include a "Current contact" checkbox).
  - The Edit button becomes **Save**, with a blue **Cancel** link below it. Save commits inputs back into the view; Cancel reverts.
- **Footer** — NSHCS / NHS England footer with link rows and legal links.

## Tech

- Plain HTML, CSS and vanilla JavaScript — no frameworks, no bundler.
- Accordion animation uses the `grid-template-rows: 0fr → 1fr` technique for height transitions.
- Date inputs format human-readable dates (`14 Mar 2022`) on save.
- System fonts only.

## File structure

```
.
├── index.html       # the design
└── README.md
```
