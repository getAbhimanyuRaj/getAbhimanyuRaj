
## 2024-10-24 - SVG Text Shadow Bloat
**Learning:** The codebase relies on duplicating massive SVG ASCII art blocks multiple times to simulate CSS text-shadow and glow effects, leading to significant file size bloat and DOM complexity.
**Action:** Always check SVGs with complex text effects for duplication. Extract these repeated blocks into a <g> tag within <defs> and reference them via <use> to drastically reduce file size while preserving visual fidelity.
