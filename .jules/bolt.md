## 2026-10-06 - deduplicating SVG with defs reduces DOM size and file size
**Learning:** Deduplicating large blocks of ASCII art text within SVGs into a `<defs>` section and using `<use>` substantially reduces file size (45% here) and DOM complexity, making the asset faster to parse and render.
**Action:** Always profile SVG assets for large repeated node blocks, particularly ASCII text or paths, and abstract them into `<defs>` before resorting to attribute-level minification.
