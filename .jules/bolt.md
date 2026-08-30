## 2024-05-18 - Deduplicating SVG Text Nodes
**Learning:** For SVG files containing repeated identical ASCII art (or large text blocks), deduplicating the nodes by moving them into `<defs>` and referencing them with `<use>` reduces file size by nearly 50% without affecting visual rendering. String manipulation in Python works well for parsing SVG with attributes like `xml:space="preserve"` when XML libraries drop them on serialization.
**Action:** Deduplicate identical massive text blocks in SVGs across the codebase using `re` and `<use>`.
