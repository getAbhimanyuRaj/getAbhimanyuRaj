## 2024-05-24 - SVG Defs Deduplication
**Learning:** Extracting heavily duplicated elements into `<defs>` and referencing them with `<use>` significantly reduces SVG file size without visual changes. Be careful when scripting replacements to avoid infinite recursive `<use>` loops (only replace instances outside `<defs>`).
**Action:** Always check heavily animated or layered SVGs for repeated blocks of XML (like text or complex paths) and refactor them into `<defs>` for a straightforward file size and parsing optimization.
