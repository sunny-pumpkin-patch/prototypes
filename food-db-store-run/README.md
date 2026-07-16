# Food-DB Store Run

Phone-first field checklist for the food-DB **barcode + UX** store test (2026-07-15).
Live: https://sunny-pumpkin-patch.github.io/prototypes/food-db-store-run/

14 aisle-ordered scans, tap Found/Miss, live hit-rate, MyFitnessPal gap question only on a
miss. State persists in `localStorage`; "Copy results" emits a paste-able block.

**Scan on the dev build** — `lookup-product` write-through caches every USDA/OFF hit, so
measuring on prod improves prod as a side effect. Three items are flagged with a brand to
avoid because dev's cache already holds them.

Source of truth for the numbers: `ops/data/food-db-test/RESULTS-2026-07-15.md`.
Generated from `ops/data/food-db-test/store-run.html` (the Claude artifact source) by
wrapping it in a standalone HTML skeleton — that file has no `<head>`/`<body>` of its own.
