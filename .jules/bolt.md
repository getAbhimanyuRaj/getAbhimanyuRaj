## 2024-05-24 - SVG Deduplication and Attribute Inheritance
**Learning:** Extracting duplicated SVG text blocks into `<defs>` and referencing them with `<use>` effectively reduces file size. Additionally, attributes like `fill` and `xml:space` can be hoisted to a parent `<g>` tag to save space, but `lengthAdjust` is not inherited by child `<text>` elements.
**Action:** Deduplicate SVG nodes into `<defs>` for heavily repeated structures and hoist inheritable attributes to parent containers to optimize file size without losing formatting.
