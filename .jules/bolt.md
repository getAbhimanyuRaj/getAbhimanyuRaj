## 2024-08-18 - SVG Attribute Inheritance Trap
**Learning:** When using Python string replace to optimize SVGs by removing redundant attributes on child elements, be careful that you don't inadvertently remove those attributes from the parent `<g>` tag if they're formatted similarly.
**Action:** When programmatically optimizing SVGs via string replacement, either add the optimized parent tag *after* stripping the redundant attributes from the entire string, or use regex/an XML parser to exclusively target `<text>` elements.
