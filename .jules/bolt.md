## 2024-05-15 - SVG Deduplication
**Learning:** Extracting large repeated chunks of ASCII art in SVGs to a `<g>` within `<defs>` and utilizing `<use href="#id"/>` dramatically reduces file size.
**Action:** Use string replacement to move deduplicated SVG blocks into `<defs>` and replace duplicates with `<use>`, but ensure to strictly replace only in the body by splitting the string at `</defs>`.

## 2024-05-15 - SVG Global Attribute Deduplication
**Learning:** Text elements in SVG inherit properties like `fill` and `xml:space` from parent `<g>` tags, saving bytes when repeated dozens of times.
**Action:** Lift common attributes to parent elements using Regex or python string replace.
