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
| Applications | Exported social avatar/profile and a small set of post graphics for intended channels; additional mockups and product screens selected from actual brand needs. No editable social templates or certificate deliverables. |
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

## Complete-kit acceptance criteria

A full kit is a collection of actual files, not a single image. Required categories: strategy, approved naming/messaging, logo family, semantic color system, licensed/qualified typography, visual language, voice, business-relevant applications, **illustrated multipage Manual de Marca PDF**, implementable technical appendix, editable sources where supported, practical exports and release manifest. Mark each category delivered, pending, excluded by scope, blocked or unverified; never claim completion while a mandatory category is missing.

- Produce the logo family from coherent masters: primary, secondary, symbol if appropriate, monochrome/reverse, small-size behavior. Document geometry, clear space, tested minimum sizes, backgrounds and prohibited uses. Check vector path editability and transparent raster exports.
- Supply role-based palette values (HEX/RGB, qualified CMYK by named profile where relevant), allowed combinations and measured contrast. Pantone matches only if verified.
- Record actual font names, weights, source/license, language coverage, fallbacks and usage hierarchy; do not redistribute restricted font files.
- Define repeatable rules for patterns, shapes, icons, illustration, photography, composition and brand voice, with on-brand/off-brand examples.
- Select applications from actual channels and provide relevant mockups **and**, when required, separately measured production layouts; distinguish each from a concept image.
- Include an asset index with filenames, paths, format, dimensions, color space if known, editable/export status, source/license, approval status and limitations. Deliver semantic digital tokens when applicable.
- Ensure all representations of the identity use the same approved master assets; do not regenerate logo lettering separately for every mockup.

## Manual-first packaging rule

A manual approval candidate contains the PDF, editable layout source where supported, technical appendix, approved/proposed source-of-truth specifications, representative draft artwork, application mockups, and a **planned production asset manifest**. It need not contain all final exports. After explicit manual approval, produce the individual production assets listed in the approved manifest and validate them. Label draft masters and mockups separately from final exports; no final package may be called delivered at Gate A. Use [asset-production.md](asset-production.md) for technical standards.

## Core social exports and optional application groups

For complete kits, deliver actual social graphics, not only copy or pictures of posts inside the manual. Define channels, dimensions, content and export formats in the inventory; verify current channel specifications when relevant. Editable social templates and certificates are excluded from this skill's deliverables. This does not remove editable logo masters or manual sources.

Choose additional mockups and product screens by business context, audience, workflows and devices. A physical-product brand may need packaging mockups; a software brand may need relevant interface screens. Neither implies a fixed collateral list or a working application. Scope real exports separately from illustrative mockups. Standalone Markdown brand/product/voice guides and page-image previews may be added when useful; they do not replace required manual or asset files.

For Lovable projects, offer the optional implementation kit under [lovable-handoff.md](lovable-handoff.md). Selection adds its concrete files to the manual-first inventory, not automatic permission to produce final assets before Gate A.
