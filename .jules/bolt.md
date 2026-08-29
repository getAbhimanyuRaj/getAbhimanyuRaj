## 2024-08-29 - SVG Commenting vs File Size Reduction
**Learning:** When attempting to optimize SVGs by extracting repeated `<text>` to `<defs>`, adding mandatory explanatory comments counteracts some of the file size reduction goal.
**Action:** Always include the required explanatory comment as an XML comment (e.g., `<!-- Optimization: ... -->`) inside the SVG, even if it slightly increases file size, to comply with strict documentation rules.
