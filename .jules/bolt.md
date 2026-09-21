## 2024-10-18 - SVG Deduplication with <use> tags
**Learning:** Extracting massive duplicated ASCII art or text blocks into a `<g>` tag within `<defs>` and referencing them with `<use href="#id"/>` can significantly reduce file size (in this case, almost 50% reduction for `name-banner.svg`).
**Action:** Always search for identical, heavily repeated blocks in SVG assets (especially animated ones) and abstract them into `<defs>` to save bandwidth without sacrificing visual fidelity.
