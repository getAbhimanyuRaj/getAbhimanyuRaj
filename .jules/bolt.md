## 2026-11-04 - SVG ASCII Art Deduplication
**Learning:** Found that this codebase heavily duplicates large ASCII art blocks within SVG files to create shadow/glow effects (3 times in `name-banner.svg`). This significantly inflates file size and DOM complexity.
**Action:** Extract the repeated block into a `<g>` tag within the `<defs>` section and reference it using `<use href="#id"/>`. Ensure to verify identical blocks first.
