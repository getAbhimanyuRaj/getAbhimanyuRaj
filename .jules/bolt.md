## 2024-10-31 - SVG ASCII Art Duplication
**Learning:** SVGs in this codebase often duplicate massive ASCII art blocks multiple times to simulate CSS text-shadow and glow effects. These should be deduplicated by extracting them into a `<g>` tag within `<defs>` and referencing them via `<use>` to prevent file bloat.
**Action:** Extract repeated text blocks to `<defs>` and reference them via `<use>` elements instead of duplicating the entire block, taking care not to place hardcoded styles inside `<defs>` so they can inherit properly.
