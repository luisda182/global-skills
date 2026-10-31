# Validation and accessibility

Read for every themed output. These are practical design gates; passing them is not a claim of complete WCAG, PDF/UA or other formal conformance.

## Checks before delivery

1. **Source integrity:** compare text, question numbers and marks, equations, data, labels, citations, links, notes, hidden slides, and protected school elements against the source. For new artifacts compare against the supplied content specification. Treat changes introduced by styling as defects. Check student-facing exports for accidentally exposed solutions.
2. **Style:** verify chosen theme and scoped overrides, actual installed fonts, missing glyphs, consistent semantic roles and source page/slide geometry. Inspect after fallback substitution.
3. **Contrast:** calculate foreground/background relative-luminance contrast for every used pairing, including text on fills and image overlays. Target at least 4.5:1 for all ordinary theme text; large text can meet WCAG AA at 3:1 (18 pt regular or 14 pt bold), but this package deliberately targets 4.5:1 even there. Essential graphical objects should reach 3:1 against adjacent colors. Avoid rounding a near-failing ratio upward.
4. **Meaning and structure:** ensure no hue-only instructions or categories, logical reading order, alt text, actual headings and table headers, editable content where supported, descriptive hyperlinks, and unique descriptive slide titles. Use the authoring application's checker when available; record unsupported checks.
5. **Visual proof:** render every final page/slide, then inspect for clipping, overlap, lost symbols, broken equations, tiny labels, split questions, inadequate answer space, table overflow, missing letterhead and inaccurate chart rendering. Inspect exported files as well as the editable source where an export is requested. Re-render affected output after changes.
6. **Grayscale proof:** mandatory for Theme 1 and any requested print variant. Render at intended paper/handout size and inspect all pages in grayscale. Distinguish all series and statuses without hue; check thin lines and source images. A monochrome palette alone is insufficient. Note whether only a digital proof or a physical sample was checked.
7. **Completion:** state pass/fail/not checked for integrity, contrast, visual proof, accessibility checker and grayscale (or not applicable). Fix failures within scope; disclose unresolved issues and tool limitations. Do not describe an artifact as fully validated if required checks could not run.

## Contrast method

For each sRGB channel c in [0,1], use c/12.92 when c ≤ 0.04045, otherwise ((c+0.055)/1.055)^2.4. Relative luminance L = 0.2126R + 0.7152G + 0.0722B. Contrast = (lighter L + 0.05)/(darker L + 0.05). Transparency and actual backgrounds must be resolved before calculation. Ratios do not establish grayscale separability between chart series; labels and proofing remain necessary.

## Authoritative references

Consulted 2026-10-31. WCAG is a web standard; these criteria inform the package's document and slide design targets rather than certifying an exported file.

- [W3C: Contrast (Minimum), SC 1.4.3](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html): text contrast thresholds and large-text definition.
- [W3C: Use of Color, SC 1.4.1](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html): visible alternatives to hue-only information.
- [W3C: Non-text Contrast, SC 1.4.11](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html): meaningful graphical objects and adjacent-color contrast.

The font sizes, margins, palettes and layout choices in this package are proposed local defaults, not requirements quoted from W3C or an official school policy.
