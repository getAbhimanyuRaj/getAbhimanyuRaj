## 2024-05-24 - SVG Deduplication Pitfalls
**Learning:** When using Python to deduplicate SVG nodes into <defs> via string manipulation, doing a global replacement without splitting the file at </defs> can accidentally replace the source block inside <defs>, causing an infinite <use> recursion loop.
**Action:** Always split the document content (e.g., at </defs>) and apply string replacements for deduplication only to the document body.
