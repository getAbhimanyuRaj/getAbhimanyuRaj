
## 2024-05-18 - Targetting XML Attributes
**Learning:** When programmatically removing XML attributes (like `fill` or `xml:space`) from child elements via string replacement, doing so globally *after* injecting those same attributes into the parent container will inadvertently strip them from the parent as well.
**Action:** Always split the document content (e.g., around the parent tag) and apply attribute-stripping string replacements *only* to the section containing the children (the tail).
