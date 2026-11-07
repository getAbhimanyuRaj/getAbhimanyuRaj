
## 2026-11-07 - Deduplicating SVG ASCII Art
**Learning:** Extracting duplicated SVG blocks to `<defs>` and referencing them via `<use>` significantly reduces file size while preserving styling inheritance from parent `<g>` tags.
**Action:** Use this technique for any SVG heavily duplicating ASCII art to optimize size without breaking layout.
