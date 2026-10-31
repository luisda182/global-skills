# Quality review and release

Inspect deliverables at intended size before seeking acceptance. Use available rendering/preview tools for PDF, presentation, document, image, and vector outputs. If a format cannot be rendered, record it as unverified; do not claim it passed visual inspection.

## Review criteria

- Identity integrity: correct business, approved direction, exact name spelling, consistent palette/font/logo versions, no other business's assets or facts.
- Logo: visual balance, distinctiveness relative to reviewed references, small-size readability, clear space, unclipped exports, expected transparency, coherent monochrome and reverse versions. Distinctiveness review is not legal clearance.
- Color: calculate contrast for intended text pairs. Target at least 4.5:1 for normal text and 3:1 for large text (18 pt regular or 14 pt bold) under WCAG AA; check meaningful interface graphics at 3:1 where applicable. Do not imply a palette proves an entire product accessible. Verify current authoritative criteria when making formal compliance claims.
- Type: actual family/weight or documented substitution, readable hierarchy, supported characters, no missing glyphs, overflow, or unintended line breaks.
- Applications: fit to the business and medium, correct dimensions and safe areas, consistent voice and spacing, working editable sources and expected exports. Verify current platform specifications when relevant.
- Packaging: open real files, check relative paths, semantic token values, manifest coverage, version/status, source and license notes. Do not claim font or trademark rights without evidence.

For a complete manual, use the page-level review in [brand-manual.md](brand-manual.md) and the asset/value checks in [technical-appendix.md](technical-appendix.md). Verify that the central concept is recognizable across the name, mark, palette, typography, imagery, voice and applications. Resolve mismatches instead of explaining away unrelated elements.

## Approval and revision

Present a release candidate with a concise review result, previews, delivered formats, unresolved limitations, and the exact version for acceptance. Draft status must remain visible until approval. Only block acceptance on meaningful unresolved requirements; optional additions can be listed separately.

Record user acceptance or explicit delegated authority in the decision log, update the release manifest and business record, and preserve the accepted version. If changes are requested, keep acceptance scoped: approval of a palette does not approve an unrelated logo. A rejected direction remains rejected unless the user reopens it.

For a later rebrand, retain the prior accepted release, identify affected outputs, and create a migration note describing the approved replacements. Do not silently rewrite the existing source of truth.

## Mandatory release gates and failure conditions

Before declaring a complete brand kit or Manual de Marca ready:
1. **Existence:** verify the real PDF, layout source (or explicit exception), technical appendix, logo masters/exports, selected applications and manifest. Never substitute a single image or written promise.
2. **Coverage:** check every required chapter and kit category against the approved brief; note exclusions, blockers, drafts and missing items explicitly.
3. **Page inspection:** render and visually inspect **every PDF page** at readable scale for overflow, clipping, missing fonts/glyphs, image problems, layout rhythm, captions, page numbers and contents references; re-render fixes.
4. **Asset integrity:** open representative files and verify SVG paths/viewBox, PNG transparency, intended dimensions, color roles, logo consistency, source editability and file paths.
5. **Technical accuracy:** recompute color contrast and validate values, measurements, type licensing evidence, qualified print conversions and matching tokens. Unknown or simulated specifications must be labeled.
6. **Evidence integrity:** remove unverified trademark/domain/social availability checkmarks, fabricated business/customer claims, fictitious contact information, untested legal or compliance statements.
7. **Brand coherence:** compare the approved concept against name, mark, palette, type, graphics, voice and applications; correct off-system assets.
8. **Handoff:** provide versioned files and manifest, review results, known limitations, and an explicit acceptance request. Do not mark approved until accepted.

Use a pass/fail/unverified result for each gate. A mandatory failed or unverified item blocks a **complete/production-ready** claim; deliver an accurately labeled draft or partial release instead. Do not assert inspection was performed unless files were actually inspected.

## Two acceptance gates

**Gate A — Manual approval:** validate the actual multipage PDF and coherent draft masters, strategy/name/direction alignment, technical specifications, and proposed production inventory. Ask for explicit acceptance of the identity system. Do not require all final export files at this gate.

**Gate B — Asset release approval:** after Gate A, produce and verify every approved final asset or mark a documented exception. Check vector masters, PNG/PDF exports, dimensions, print profiles, licenses, manifest, consistency with the accepted manual and file integrity. Ask for explicit production release acceptance. Never describe Gate A as final asset delivery or Gate B as automatic.
