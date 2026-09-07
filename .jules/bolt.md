
## 2024-05-24 - SVG <use> Recursion and Deduplication
**Learning:** Deduplicating large repetitive text blocks in SVGs (like ASCII art) into `<defs>` and referencing them with `<use>` dramatically reduces file size. However, doing this via naive global string replacement can replace the definition block itself inside `<defs>`, causing an infinite recursion rendering bug.
**Action:** When programmatically modifying SVG strings to deduplicate nodes, always split the document around `</defs>` and only apply replacements to the main document body.
