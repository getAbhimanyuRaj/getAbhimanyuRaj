
## 2024-10-08 - SVG Text Deduplication and `<use>` Inheritence
**Learning:** When extracting massive blocks of `<text>` elements to `<defs>` to deduplicate an SVG (using `<use href="#id"/>`), formatting attributes like `xml:space="preserve"` and length adjustments need to be kept on the `<text>` elements themselves. However, style attributes (like `fill` or `opacity`) on the parent `<g>` tags wrapping the `<use>` tags correctly propagate into the Shadow DOM as long as the original definitions don't have hardcoded styles overriding them.
**Action:** When extracting repeated chunks in SVG, strip the context-specific wrapper styles (like `fill="url(#base)"`) from the defs version, leaving it "bare", so that the wrapper `<g>` around the `<use>` tag can apply its unique styles dynamically.
