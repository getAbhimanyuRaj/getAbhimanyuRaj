## 2024-09-14 - SVG DOM Node Deduplication
**Learning:** Extracting massively duplicated internal nodes (like ASCII art `<text>` blocks) into `<defs>` and referencing them with `<use>` drastically reduces SVG file size and parsing time without changing functionality, provided the parent groups inject the necessary distinguishing attributes (e.g. `fill`).
**Action:** Always search for highly duplicated chunks of XML/SVG before attempting global property hoisting.
