---
name: swopcase-asset-briefing
description: Generate SwopCase image, UGC, video, GIF, and placeholder asset plans with exact filenames, dimensions, prompts, creator briefs, and replacement instructions for Shopify themes.
---

# SwopCase Asset Briefing

Use this skill whenever the theme needs visuals, placeholders, UGC directions, GIF loops, or image-generation prompts.

## Core rule
Do not generate real visuals directly in-theme.
Instead, define the asset system precisely so the operator can create or source the final assets later.

## For every asset, always output all fields below
- `SECTION:`
- `ASSET NAME:`
- `FILE NAME:`
- `TYPE:` one of `KI-Bild`, `KI-Video/GIF`, `UGC-Foto`, `UGC-Video`, `Placeholder`
- `DIMENSIONS:` exact pixel size
- `PLACEMENT:` where it appears in the theme
- `WHY IT EXISTS:` conversion purpose
- `PROMPT / BRIEF:`
- `PLACEHOLDER FILE:` matching SVG filename if applicable
- `REPLACEMENT NOTE:` how final asset should replace placeholder

## Asset sizing defaults
- Hero Desktop: `1440x800`
- Hero Mobile: `750x900`
- Product Grid Tile: `800x1000`
- Lifestyle/Ambiance: `1200x800`
- UGC Square: `600x600`
- UGC Portrait: `1080x1350`
- Reel / Vertical Video: `1080x1920`
- GIF Loop: `800x800`

Always override defaults only when layout requires it.

## KI-Bild rules
- Max 120 tokens.
- Ready for OpenAI image generation.
- Prioritize product readability and believable composition.
- End prompt with:
`warm soft side light, background #F1E9E9, satin surface, clean minimal, no human faces, lifestyle aesthetic, phone case visible`

## UGC-Foto rules
Always provide:
1. `CREATOR BRIEF:` what the human should shoot.
2. `VISUAL REFERENCE PROMPT:` a KI still prompt to create a reference mockup for the creator.

The creator brief must specify:
- framing
- hand pose or body crop
- light source
- styling
- props
- what part of the case/swop must be visible
- desired mood

## UGC-Video rules
Always provide:
1. `CREATOR BRIEF:`
2. `SHOT LIST:`
3. `VISUAL REFERENCE PROMPT:`

The brief must specify:
- duration
- aspect ratio
- movement
- action beats
- environment
- styling
- product interaction

## GIF / loop rules
Treat GIF loops as production assets.
Always provide:
1. `PRODUCTION BRIEF:`
2. `SHOT LIST:`
3. `VISUAL REFERENCE PROMPT:`
4. `NOTE: ECHTES MATERIAL ERFORDERLICH – nicht final per KI rendern` when product accuracy matters.

## Placeholder SVG rules
If a visual is not available yet, provide a placeholder SVG spec:
- file name: `placeholder-[asset-name].svg`
- exact final dimensions
- background: `#D9CDCD`
- centered label with asset name and size
- short asset type label

## Output format
Return assets in a numbered list.
Be concise but production-ready.
