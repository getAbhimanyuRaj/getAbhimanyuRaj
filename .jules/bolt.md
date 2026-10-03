## 2024-10-03 - SVG Attribute Inheritance Insight
**Learning:** SVG attributes like `lengthAdjust` are not inherited by child elements from parent `<g>` groups, unlike styling properties such as `fill` or `xml:space`.
**Action:** When hoisting common SVG attributes to parent groups to reduce file size, strictly filter the properties to only those known to natively inherit (presentation attributes like colors, typography, or spatial preservation flags).

## 2024-10-03 - Efficient String Replacement for SVG Defs Deduplication
**Learning:** Performing a global string replacement to substitute duplicated visual blocks with a `<use>` tag reference can accidentally overwrite the newly extracted source block inside the `<defs>` container, causing recursive referencing bugs.
**Action:** Always slice the SVG markup string (e.g., using `content.find('</defs>')`) into `head` and `tail` sections. Apply `<use>` replacements exclusively on the `tail` section (the document body).
