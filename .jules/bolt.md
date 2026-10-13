## 2024-10-13 - SVG Asset Size Optimization
**Learning:** For heavily duplicated blocks in SVGs (like large ASCII art in a static profile README), extracting the repeated segment to a `<defs>` node and referencing it via `<use>` is an effective way to significantly reduce file size and DOM complexity without introducing new runtime dependencies or architectural changes.
**Action:** Always check raw SVG files for heavy duplication as low-hanging fruit for bandwidth/parsing optimization, and ensure the extracted segment is large enough to justify the minimal overhead of the wrapper tags.
