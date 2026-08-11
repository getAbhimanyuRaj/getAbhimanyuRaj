## 2024-05-24 - SVG Text Duplication Anti-Pattern
**Learning:** The codebase's SVGs use a pattern of duplicating large blocks of `<text>` elements multiple times to achieve layering and glow effects, significantly inflating file size and DOM complexity.
**Action:** Always refactor repeated SVG blocks into `<defs>` and reference them via `<use>`, applying layer-specific styles (like `fill` and `filter`) on the `<use>` element itself.
