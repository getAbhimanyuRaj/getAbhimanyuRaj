
## 2023-10-21 - SVG Node Deduplication with `<use>`
**Learning:** Extracting large repeated nodes (like complex ASCII art wrapped in `<text>` tags) into an `<id>`-tagged group inside `<defs>` and referencing them with `<use>` can massively reduce file sizes and DOM complexity in SVGs. However, it's critical to isolate the `<use>` string replacements to the document body to prevent replacing the newly extracted source node inside `<defs>`, which would cause infinite recursion.
**Action:** Always split the SVG string (e.g., around `</defs>`) before applying global replacements for deduplication, and verify the resulting structure with an XML parser.
