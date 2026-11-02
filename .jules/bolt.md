## 2024-05-14 - SVG Asset Bloat
**Learning:** SVG files in this static README (like name-banner.svg) duplicate massive ASCII art text blocks multiple times (3x) to simulate CSS text-shadow and glow effects, significantly bloating file size. Standard tools like React's optimization tricks are inapplicable here.
**Action:** Always verify if repeating text/nodes can be extracted into `<defs>` and reused via `<use>`, ensuring to split the content safely so `xml:space` is preserved and recursion avoids infinite loops.
