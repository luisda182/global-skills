# Asset production — standards and post-manual workflow

This reference applies **after explicit Manual de Marca approval (Gate A)**. Working draft assets used to construct the manual are not the final production package. Generate only the assets specified in the accepted manual and production manifest. If production reveals a required identity change, return it for scoped manual approval before proceeding.

## Authoritative technical references

Consult current specifications when relevant and record the version, date, URL and applicable requirements:
- W3C SVG 2: https://www.w3.org/TR/SVG2/ — valid editable vector graphics, viewBox and rendering.
- W3C WCAG 2.2: https://www.w3.org/TR/WCAG22/ — digital contrast and accessibility checks.
- W3C CSS Color 4: https://www.w3.org/TR/css-color-4/ — digital color definitions.
- International Color Consortium: https://www.color.org/ — color profiles and managed conversion.
- Adobe brand guidelines overview: https://www.adobe.com/creativecloud/design/discover/brand-guidelines.html — contextual design guidance, not a technical standard.

Links are reference starting points, not proof that a design complies. Confirm any printer-specific PDF/X, dieline, bleed, finishing, substrate or spot-color requirements with the actual vendor. Do not claim Pantone matches, trademark rights, font licenses, or profile compliance without evidence.

## Production sequence

1. Read the approved manual, source-of-truth design values and asset inventory; freeze version and scope.
2. Inventory draft masters and source files; refine approved artwork into reproducible editable masters, preserving approved geometry and type treatment.
3. Export each approved variant in specified formats and sizes. SVG masters must contain genuine vector paths; PNG files must have correct transparency, pixel size and resolution; print PDFs must use documented color settings.
4. Produce application-specific files (menus, packaging, signage, social templates, uniforms) only when listed, using actual vendor/platform specifications.
5. Verify fonts, license sources, language glyphs, accessible color combinations, dimensions, safe areas, file opening, SVG viewBox/clipping and cross-format consistency.
6. Populate manifest: path, purpose, format, dimensions, color profile, master/export distinction, rights, version, validation result and exceptions.
7. Deliver the package for **Asset Release Gate B**. Do not label unverified outputs production-ready.

Use one master for each logo configuration; do not independently regenerate marks for separate mockups. Maintain an issue log and rerun relevant checks after corrections.
