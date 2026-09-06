## 2024-09-06 - SVG DOM Tree Optimization
**Learning:** In purely static repositories containing massive ASCII art SVGs (like `name-banner.svg`), repeated text blocks create enormous DOM bloat and file size overhead.
**Action:** Always extract static ASCII text blocks into `<g>` tags within `<defs>` and re-use them via `<use href="#id"/>`. This cuts file size nearly in half without breaking inherited styling gradients.
