## 2024-10-23 - SVG Deduplication Pitfalls
**Learning:** When programmatically modifying SVG files, using global string replacement to extract content to `<defs>` can inadvertently replace the source node within `<defs>` if not careful, leading to an infinite `<use>` recursion loop. Also, `lengthAdjust` is not inherited by child `<text>` elements.
**Action:** Always split the SVG content (e.g. around `</defs>`) and only apply replacement logic to the body. Keep non-inheritable attributes on the `<text>` elements within `<defs>`.
