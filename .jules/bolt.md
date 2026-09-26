## 2024-10-26 - SVG Optimization Using <use> tags

**Learning:** When optimizing SVG files containing duplicated elements (like ASCII art), extracting the duplicated block into a `<g>` tag within `<defs>` and reusing it with `<use>` tags significantly reduces file size and DOM node count without visual changes. Elements instantiated via `<use>` correctly inherit styling properties in their shadow DOM from the parent `<g>`, provided the original `<defs>` elements lack hardcoded styles.

**Action:** Before optimizing SVGs via `<defs>`, always confirm actual duplication count using tools like `grep` to ensure the overhead of `<defs>` isn't greater than the savings. Ensure proper XML validation of the output using Python scripts when standard linters are unavailable.
