
## 2024-05-18 - SVG Code Duplication and Size Optimization
**Learning:** Heavy use of text shadowing or glows in SVGs (like `name-banner.svg`) often duplicates massive text blocks (like ASCII art) verbatim. Extracting the duplicated nodes into a `<defs>` block and referencing them with `<use href="#id"/>` cuts down the file size by nearly half and simplifies the DOM, without losing visual fidelity since styling inherited from wrapper `<g>` tags is preserved in the shadow DOM.
**Action:** Whenever multiple identical `<text>` or path sequences appear in an SVG for layering effects, extract them into a `<g>` within `<defs>` and substitute the originals with `<use>` tags.
