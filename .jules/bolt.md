## 2023-10-30 - SVG deduplication pattern
**Learning:** For SVGs containing large ASCII art used multiple times for visual effects (glow, shadow), extracting the block to `<defs>` and reusing with `<use>` drastically reduces file size and parser overhead while keeping visuals intact.
**Action:** Always check heavily repeated structural SVG nodes to see if they can be moved to `<defs>` and `<use>`d instead of copying raw XML.
