# Bolt's Journal

## 2026-09-22 - SVG Deduplication for Static Assets
**Learning:** For static repositories consisting primarily of complex SVG assets (like ASCII art), significant performance gains (file size and DOM complexity reduction) can be achieved by deduplicating exact repeated blocks of `<text>` elements. By moving the base block into a `<defs>` group and referencing it with `<use href="#id"/>`, the SVG file size can be slashed substantially (e.g., ~45% reduction) while perfectly retaining visual rendering.
**Action:** When auditing static SVGs, specifically look for layered effects (glows, drop shadows, duplicate animations) that re-declare identical text/path structures. Extract the base geometry into `<defs>` to optimize parsing speed and memory usage.
