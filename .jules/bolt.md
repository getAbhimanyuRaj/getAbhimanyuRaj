## 2024-09-25 - SVG Optimization Limits

**Learning:** Extracting duplicated SVG blocks to `<defs>` and referencing via `<use>` only yields file size reductions when the block is heavily duplicated. For single occurrences, the wrapper overhead actually increases file size.

**Action:** Always measure duplication count (e.g. via `grep -c` or python string counts) before implementing `<defs>` extraction to guarantee a measurable performance/size win.
