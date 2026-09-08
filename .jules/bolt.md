## 2023-10-25 - SVG Size Optimization via Defs Deduplication
**Learning:** Repetitive inline ASCII art blocks in SVGs greatly inflate file size. Extracting common text structures into `<defs>` and utilizing `<use>` keeps rendering intact while drastically reducing byte count.
**Action:** When working on profile README static assets, target SVG deduplication (using targeted string replacement/Regex to preserve spacing elements like `xml:space="preserve"`) for immediate performance improvements.
