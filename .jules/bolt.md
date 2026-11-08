## 2024-11-08 - SVG DOM Complexity Optimization
**Learning:** The SVGs in this codebase duplicate massive ASCII art blocks multiple times to simulate CSS text-shadow and glow effects, leading to significant file bloat and DOM complexity.
**Action:** Extract these blocks into a `<g>` tag within `<defs>` and reference them via `<use>` to prevent file bloat while maintaining styling inheritance.
