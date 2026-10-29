
## 2024-10-29 - Deduplicating SVG Text Blocks
**Learning:** SVG files generated for GitHub profiles frequently duplicate large `<text>` blocks to simulate drop shadows, glows, and other composite effects. The `<use>` tag correctly inherits properties in its shadow DOM from the parent `<g>` only if the referenced elements in `<defs>` lack hardcoded styles (like `fill`).
**Action:** Extract heavily duplicated content (like ASCII art) into `<defs>`, ensuring it does not have hardcoded styling that would override parent `<g>` styling contexts, and replace the duplicates with `<use href="#id"/>`. Wait, in this case, the `fill` is applied to the parent `<g>`, and the `<text>` blocks themselves don't have a `fill` attribute, so inheriting the color from `<g>` when using `<use>` works perfectly.
