## 2024-08-12 - SVG Asset Optimization
**Learning:** For repos consisting mostly of static SVG assets, file size optimization through native SVG constructs like `<defs>` and `<use>` is highly effective for reducing duplication and footprint without modifying the underlying UI rendering.
**Action:** When inspecting static SVG assets, look for heavily repeated blocks (e.g. large text or complex path groups) and extract them to a reusable definition.
