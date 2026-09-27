## 2024-09-27 - Deduplicating static SVG text elements using `<defs>`
**Learning:** Extracting massive, duplicated static text blocks (like ASCII art) into `<defs>` and rendering them with `<use>` effectively avoids infinite recursion loops and preserves layout formats when manipulated via targeted string replacements (rather than fully serialized XML, which risks losing spacing configurations).
**Action:** Always verify exactly what requires updating in static assets and construct isolated test environments via scripting before editing full structures.
