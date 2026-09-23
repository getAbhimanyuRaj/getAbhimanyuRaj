## 2023-10-25 - SVG Size Optimization Pattern
**Learning:** In static repositories using large SVG files with repeated ASCII text nodes, standard minimization doesn't solve the core redundancy issue. The `<defs>` tag and `<use>` elements offer a massive reduction in file sizes (e.g. 47% reduction observed) by deduplicating exact matches inside the DOM directly, while still inheriting styling cascaded from outer `<g>` wrappers.

**Action:** Before trying global regex replacements or complex minifiers, always measure duplicate tags in SVG. If heavy duplication exists (especially with text blocks), extract the common nodes to a `<g id="...">` within `<defs>` and implement `<use href="#..."/>` where appropriate to optimize payloads.
