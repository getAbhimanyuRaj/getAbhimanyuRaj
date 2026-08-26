## 2024-05-18 - SVG Recursion Pitfall
**Learning:** When extracting nodes into `<defs>` and replacing them in the document body using string replacement (`replace`), it's incredibly easy to accidentally replace the newly extracted source node *inside* `<defs>` as well. This creates a `<use href="#id"/>` referencing itself, breaking the SVG with infinite recursion.
**Action:** When performing string manipulation for SVG deduplication, explicitly split the document into definitions vs. body (e.g., around `</defs>`), and only apply the string replacement to the body portion.
