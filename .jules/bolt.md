## 2024-08-16 - SVG Attribute Inheritance Insight
**Learning:** In SVGs, presentation attributes (like `fill` and `font-family`) and XML attributes (`xml:space`) can be safely hoisted to a parent `<g>` tag to reduce file size. However, the `lengthAdjust` attribute on `<text>` elements is NOT inherited and must remain on the individual `<text>` tags. Removing it breaks visual layout.
**Action:** When optimizing SVGs by hoisting attributes, verify the SVG specification for attribute inheritance (especially for text properties) to avoid visual regressions.
