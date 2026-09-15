# Oxford Graduate — Course Hero Tabs

Course hero explorations for the Oxford course page, imported from the
Claude Design project "Oxford".

## Files

- `Course Hero Tabs.html` — the prototype. Self-contained page with a
  preview switcher (Desktop / Mobile, scenario Open / Closed) around
  embedded hero variants.
- `image-slot.js` — `<image-slot>` web component used for fillable image
  placeholders.
- `assets/logo-oxford.svg` — 80×80 university square logo.
- `assets/balliol-crest.png` — college crest used in the UG hero.
- `assets/balliol-hero.png` — Broad Street facade photograph (1788x660).

## Undergraduate only

The prototype renders the undergraduate College hero (Balliol College:
UCAS campus code, founding date, student numbers, admissions contact and
open days, over a credited facade photograph).

The level is locked to `ug` in the page script, so neither a stored
`oxford-hero-tabs` localStorage entry nor a `?level=pg` query parameter
can fall back to the postgraduate hero. The PG code paths remain in the
file but are unreachable.

## Preview controls

- **Desktop / Mobile** — renders the hero in a laptop or phone frame.
- The scenario switcher (Open / Closed) is hidden at UG level; it applies
  only to the PG hero.
- `?embed=1` strips the surrounding chrome and renders the bare hero,
  which is what the preview frames load.

## Design tokens

Colours are declared as CSS custom properties taken from the Figma file:
teal `rgb(21,97,109)`, card teal `rgb(23,86,98)`, gold `rgb(242,210,94)`,
cream `rgb(254,250,236)`, navy `rgb(0,33,71)`. Type is DM Sans with
Tiempos Headline / Source Serif 4 for display.

## Running

Any static server from the repo root, e.g.

    python3 -m http.server 8765

then open <http://localhost:8765/Course%20Hero%20Tabs.html>.
