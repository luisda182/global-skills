# Brand kit production specification

For a full kit, cover every category below. Adapt formats and application choices to the business. Do not generate irrelevant collateral simply to fill a list. Record delivery, exclusions, and blockers in a manifest.

| Category | Required coverage for a full kit |
| --- | --- |
| Strategy | Business overview, audiences, positioning, promise, values, differentiators, personality, rationale |
| Naming and messaging | Approved name and usage; generate/select a name when needed using [naming.md](naming.md); tagline options/selection, value proposition, short and long descriptions, message pillars and proof points |
| Logo system | Symbol, logotipo (wordmark), primary lockup, secondary arrangement, standalone symbol where meaningful, monochrome and reverse versions; clear space, minimum size, backgrounds, misuse examples |
| Color | Named functional roles; HEX and RGB; approved combinations; text contrast results; print specifications or explicitly provisional CMYK with profile limitations |
| Typography | Display/heading/body roles as needed; families, weights, hierarchy, spacing, language coverage, fallbacks, font source and license information |
| Visual language | Shapes, patterns, composition and spacing, imagery/art direction, illustration and icon rules, representative examples |
| Voice | Voice attributes, tone by context, terminology, do/don't examples, sample headline, product description, social copy, and customer response |
| Applications | Prioritized real applications, normally business card, social avatar/post, stationery, and presentation cover/content; tailor choices to the brief |
| Guidelines | Illustrated brand manual with coherent editorial layout, rules and application examples, version/status and asset index; editable layout source plus reviewed PDF; see [brand-manual.md](brand-manual.md) |
| Technical appendix | Implementable logo/color/type/production specifications, verified contrast pairs and asset links, plus digital tokens and states when relevant; see [technical-appendix.md](technical-appendix.md) |
| Asset package | Editable masters, available exports, templates, tokens, provenance/license notes, delivery manifest and known limitations |

Copy [release-manifest.json](../assets/release-manifest.json) into each candidate release and fill it as files are produced.

## Production details

### Logos and exports

Create real editable vector masters when suitable and supported. Deliver SVG and transparent PNG exports at useful, labeled sizes; PDF for print when supported. Keep text rendering portable with outlined logo text or documented font dependencies; retain an editable source. Check SVG viewBox, clipping, and supported shapes. Never wrap a bitmap in SVG and describe it as vector artwork. Mark AI-generated raster marks as concept assets pending vector refinement when applicable.

Define clear space using a repeatable feature of the mark. Determine minimum size by checking legibility at actual output size. Show light, dark, single-color, and small-size behavior. Use precise business-name spelling in all lockups.

### Color and typography

Assign semantic roles such as background, surface, primary text, muted text, action, and accent. Specify functional status colors only if needed. Include permitted foreground/background combinations; a palette alone is insufficient.

Provide HEX/RGB for digital use. Specify a print profile when providing CMYK; without one, label conversions approximate and require proofing. Do not invent Pantone matches. Verify font availability and language coverage. Link authoritative font/license sources when researched; do not redistribute fonts unless their license permits it. State whether fonts are installed, substituted, or merely specified.

Choose hierarchy by medium, using relative scales for responsive use and concrete sizes for actual templates. Supply fallbacks and explain substitutions that materially alter the look.

### Packaging

Use business-local folders such as `strategy/`, `logos/`, `colors/`, `typography/`, `visual-language/`, `voice/`, `templates/`, `guidelines/`, and `sources/` within the candidate release as needed. A coherent package is more important than fixed folder names.

Provide design tokens in JSON or CSS for digital brands, with semantic names mapped to actual values. Do not insert guessed values into approved tokens. Include file paths, formats, purpose, version, status, source/license details, and limitations in the manifest. A specification, a preview, an editable template, and a production export must be labeled distinctly.
