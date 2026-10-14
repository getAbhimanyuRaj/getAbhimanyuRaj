## 2024-10-14 - SVG ASCII Art Duplication
**Learning:** Found a specific performance anti-pattern in static SVGs where identical multi-line ASCII art text blocks are duplicated multiple times to create visual layers or glows.
**Action:** When working with layered SVGs, extract the identical duplicate `<text>` blocks into `<g id="content">` inside `<defs>` and reference them via `<use href="#content"/>` to cut file size by up to 50% and reduce DOM tree complexity, while preserving all styling logic.
