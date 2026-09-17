
## 2024-05-23 - SVG Size Optimizations
**Learning:** Deduplicating ASCII art text into a `<defs>` section and referencing it via `<use>` heavily reduces file size and DOM complexity for GitHub Readme SVGs, especially when the duplicated text blocks are large. In addition, common attributes like `xml:space="preserve"` and `fill="#ffffff"` are correctly inherited by child `<text>` nodes from a `<g>` wrapper, which drastically cuts down on redundant markup in files with many text lines.
**Action:** Always search for large duplicate elements (e.g., repeating groups of shapes or text) in SVGs that can be moved to `<defs>` and reused via `<use>`. Similarly, extract repeated attributes from child elements and place them on a common parent container (like `<g>`) when inheritance applies.
