## 2024-05-24 - SVG Deduplication via DEFS
**Learning:** This static repository uses SVGs as primary visual assets. Inline, duplicated text elements in SVGs (often used for drop shadows, glows, or animation layers) significantly inflate file size and parsing time without adding visual value.
**Action:** Always check SVGs for structurally identical duplicated blocks (like repeated `<text>` or `<path>` elements) and extract them into `<defs>`, referencing them with `<use>`.
