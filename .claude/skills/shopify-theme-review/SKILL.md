---
name: shopify-theme-review
description: Review Shopify OS 2.0 theme changes for SwopCase with focus on Liquid structure, section quality, responsiveness, maintainability, conversion clarity, placeholder handling, and launch readiness.
---

# Shopify Theme Review

Use this skill whenever reviewing theme code, proposed edits, or release readiness.

## Review goals
Evaluate whether changes are:
- safe to merge
- compatible with Shopify OS 2.0 patterns
- understandable for future edits
- strong for mobile commerce
- aligned with SwopCase brand and conversion needs

## Review checklist

### Liquid and schema
- Section schema is valid and organized.
- Settings are understandable to non-developers.
- Reusable sections are preferred over hardcoded one-offs.
- Blocks are used when merchant flexibility matters.

### Frontend structure
- Semantic HTML where possible.
- Avoid div soup.
- Keep CSS scoped and predictable.
- Avoid unnecessary JavaScript.

### Mobile and UX
- Mobile layout works first.
- Text remains readable.
- CTAs are visible without awkward jumps.
- Product information is scan-friendly.
- Above-the-fold communicates product and value quickly.

### Performance
- Avoid oversized media.
- Avoid animation overload.
- Lazy-load where appropriate.
- Do not introduce libraries unless clearly justified.

### Accessibility
- Alt text strategy exists.
- Buttons and links are distinguishable.
- Contrast is sufficient.
- Interactive controls are keyboard-friendly.

### SwopCase-specific checks
- Background color remains `#F1E9E9` unless explicitly working inside a bounded card.
- Placeholder assets are named consistently.
- UGC / proof / explanation layers are not removed in favor of pure aesthetics.
- The section supports cold traffic understanding.

## Output format
When reviewing, use exactly these headings:
- `PASS / FAIL`
- `CRITICAL ISSUES`
- `IMPORTANT IMPROVEMENTS`
- `NICE-TO-HAVE`
- `READY FOR PUSH?`

Be direct. If something is weak, say why.
