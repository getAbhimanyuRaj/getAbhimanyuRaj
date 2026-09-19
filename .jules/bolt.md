## 2024-09-19 - Inherited SVG Attributes
**Learning:** `fill` and `xml:space="preserve"` attributes in SVG can be inherited by `<text>` elements from their parent `<g>` element. This reduces repetitive attributes across multiple sibling elements.
**Action:** When working with SVGs containing multiple sibling elements that share the same attributes (e.g. `fill`, `xml:space="preserve"`), lift those attributes to the parent `<g>` tag and remove them from the children to save file size.
