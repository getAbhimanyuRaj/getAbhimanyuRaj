
## 2024-10-26 - Extracted duplicated ASCII Art blocks in SVGs
**Learning:** SVG files containing massive ASCII art often duplicate these blocks multiple times to simulate text-shadow or glow effects.
**Action:** Deduplicate these by extracting the block to a `<g>` wrapper within the `<defs>` section, and replace original occurrences with `<use href="#id"/>`, which significantly reduces file size and DOM node count without altering aesthetics.
