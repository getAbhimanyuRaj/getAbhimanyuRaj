## 2024-11-01 - SVG ASCII Art Deduplication
**Learning:** This codebase uses SVGs containing massive blocks of ASCII art (like `name-banner.svg`). These blocks are often duplicated verbatim within `<g>` tags to simulate CSS-like drop shadows and multi-layered glow effects.
**Action:** Extract the heavily duplicated ASCII text blocks into `<g>` tags within `<defs>`, give them an `id`, and replace the duplicated instances in the DOM with `<use href="#id"/>`. This significantly reduces file size and DOM complexity (e.g., cutting the size of `name-banner.svg` almost in half).
