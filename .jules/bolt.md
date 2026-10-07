## 2024-10-07 - SVG Data Deduplication
**Learning:** SVG files generated for profile READMEs (like `name-banner.svg`) often use exact duplication of massive `<text>` or path blocks purely for styling effects (like drop-shadows or glows via differing opacities and filters).
**Action:** Always check SVG files for large duplicated segments and extract them into `<defs>` to be reused with `<use>`. This simple deduplication dramatically cuts down file size (e.g., ~50% reduction) and DOM overhead.
