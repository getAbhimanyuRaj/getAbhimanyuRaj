## 2024-08-14 - SVG DOM Bloat in Repeated Visual Elements
**Learning:** Animated SVGs with layered visual effects (like glows or overlays) often copy-paste complex DOM nodes (e.g., text blocks) directly. This balloons file size and increases parsing overhead.
**Action:** Always check SVGs for repeated large node clusters. Extract them into a `<g>` inside `<defs>` and reference them via `<use href="#id">` to dramatically reduce file size and DOM node count without altering functionality or visuals.
