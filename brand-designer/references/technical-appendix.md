# Technical appendix / Anexo técnico

Translate the approved identity into implementable specifications. Tailor coverage to the medium: a print brand need not acquire interface states, and a software brand may need additional digital rules. Include actual values and paths, not references to a fictional brand-system website.

## Core specifications

- Logo: master filenames, symbol/wordmark/lockup relationships, coordinate system or construction geometry when useful, clear-space unit, tested minimum sizes for screen/print, small-size variants, background and monochrome rules. Ensure diagrams match actual vector paths; do not invent a decorative construction grid after the fact.
- Color: HEX/RGB, functional roles, permitted foreground/background pairs, and relevant print profiles/conversions. Provide spot-color or metallic/foil specifications only when evidenced; otherwise mark as proposed for production proofing.
- Typography: families and sources, exact weights/styles, role scales, line-height, tracking, numeric features and language coverage; fallbacks, installation/substitution status and license references. Differentiate document point sizes from responsive interface scales.
- Asset inventory: editable masters and exports, dimensions, color space/profile when known, transparency, intended use and filename conventions. State which files are concepts versus production assets.
- Production: application dimensions, safe areas, bleed/resolution requirements where relevant, paper/finish recommendations and necessary proofs. Verify requirements against the intended printer/channel rather than adopting another manual's values.

## Digital brands, when relevant

Provide machine-readable semantic tokens (JSON or CSS) using the same values as the manual. Include backgrounds, text, actions, borders and focus plus success/warning/error/information states as needed. Specify state foreground and background together, accompanying labels/icons, and light/dark variants only where actually designed. Status must not depend on color alone.

Calculate contrast using the actual exported colors and record foreground, background, ratio, applicable text/graphic role and pass/fail criteria. Refer to [quality-and-release.md](quality-and-release.md) for review criteria. Do not copy ratios or compliance claims from the reference. A result for one pair does not establish compliance for an entire interface.

Include relevant spacing, icon grid/stroke, interaction and motion specifications; provide reduced-motion behavior where motion is used. Clearly distinguish illustrative UI examples from implemented components or a working design system.

## Validation and linkage

Cross-check appendix measurements against the real assets and application examples. Ensure all token names/values agree with exports and guidelines, and all listed files exist. Label unknowns, provisional conversions and unverified production effects explicitly. Keep detailed source/license records in the package and link them from the appendix.

The appendix may be a chapter in the manual with companion machine-readable files. It does not require an additional standalone PDF. Record it as its own coverage category in the release manifest so it is not silently omitted.
