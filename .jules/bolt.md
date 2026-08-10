## 2024-08-10 - SVG Payload Optimization via `<use>` tags
**Learning:** Repetitive inline `<text>` blocks used for visual effects (like drop shadows, glowing layers, or multiple animated fills) drastically bloat GitHub profile README assets. These are duplicated completely in the DOM.
**Action:** Extract duplicate shapes/texts into `<defs><g id="...">` and reference them via `<use href="#..." />`. This reduced the `name-banner.svg` payload by ~46% without compromising visual fidelity.
