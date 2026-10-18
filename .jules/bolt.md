
## 2023-10-18 - SVG Code Duplication
**Learning:** Extracting heavy SVG text content to `<defs>` and referencing it with `<use>` only reduces file size if the text block is heavily duplicated. When deduplicating, ensure you inject the def properly to avoid recursive loops or messing up spacing.
**Action:** Always verify the duplication count before applying this technique. Use Python's ElementTree or targeted regex to parse and manipulate SVG.
