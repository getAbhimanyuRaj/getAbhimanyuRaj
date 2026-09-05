## 2024-05-15 - Initial
**Learning:** Initial setup
**Action:** none
## 2024-09-05 - SVG DOM node deduplication
**Learning:** Extracting large repeated elements (like ASCII text) into `<defs>` and referencing them with `<use>` drastically reduces SVG file size and DOM node count without altering styling applied to parent containers.
**Action:** Always check complex, layered SVGs for heavily repeated structures and deduplicate them in `<defs>`.
