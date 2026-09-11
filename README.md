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

## Levels

The page renders both admission levels, driven by a query parameter:

- `?embed=1&level=ug&scenario=open` — undergraduate (Mathematics and
  Philosophy: entry qualifications, course duration, UCAS code,
  application deadline)
- `?embed=1&level=pg&scenario=open` — postgraduate (DPhil in Ancient
  History)

`scenario=closed` shows the live-site state with applications closed.

## Design tokens

Colours are declared as CSS custom properties taken from the Figma file:
teal `rgb(21,97,109)`, card teal `rgb(23,86,98)`, gold `rgb(242,210,94)`,
cream `rgb(254,250,236)`, navy `rgb(0,33,71)`. Type is DM Sans with
Tiempos Headline / Source Serif 4 for display.

## Running

Any static server from the repo root, e.g.

    python3 -m http.server 8765

then open <http://localhost:8765/Course%20Hero%20Tabs.html>.
