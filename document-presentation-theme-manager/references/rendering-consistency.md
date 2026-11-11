# Rendering consistency

Use this workflow whenever a user requests an editable document or presentation, a preview, or a PDF/export. The goal is to preserve the selected theme and make preview/export differences small and visible; rendering engines do not guarantee pixel-identical output.

## Resolve fonts in the actual environment

1. Read the selected theme's font chains. Check the font inventory in the application and environment that will author and export the deliverable. Do not infer availability from a font name or assume a font installed on another device is available here.
2. Choose the first installed family in each chain that supports the required scripts and glyphs. Check ordinary text plus bullets, punctuation, arrows, symbols, subscripts/superscripts, and language-specific characters actually used. Keep specialist math fonts where required.
3. Apply the resolved families to document semantic styles or presentation theme/master/layout roles, including headers, tables, captions, footers and notes as relevant. Preserve each theme's design roles (for example, a serif report body with sans-serif headings). If no listed family is suitable, choose an installed, readable family with the same role and disclose the substitution. Never download or install a font without authorization.
4. Recheck line wrapping, line breaks, text fit, table widths, pagination and slide fit after substitution. Do not reduce text below the selected theme's minimum to conceal reflow.

## Use reliable list and symbol glyphs

Prefer native numbered and bulleted list features so paragraph indentation and bullet rendering travel with the editable file. Use a standard bullet such as U+2022 only after confirming it exists in the resolved font and renders in the target application. If it is missing, use a simple hyphen, numbered list, or a native shape that is part of the layout. Avoid ornamental Unicode, dingbat/Wingdings, emoji, and private-use characters for essential meaning. Verify scientific symbols and equation glyphs separately; do not replace meaningful scientific notation with visually similar but incorrect characters.

## Build paired exports from the final editable source

1. Finish and save the editable DOCX/PPTX first, including final fonts, layout, lists, images and pagination. If the task has a preview, generate or refresh that preview from this saved final source.
2. Export the PDF from that same finalized DOCX/PPTX in the same authoring workflow. Do not reconstruct a second PDF from text or create it from an earlier draft. If a requested preview is produced by a separate service, preserve the editable file and export from it, then perform the comparison below.
3. When supported by the export tool and permitted by the font license, embed fonts in the PDF. Inspect the PDF's font report/properties to confirm fonts are embedded or embedded subsets. If embedding is unavailable or cannot be verified, disclose that status; do not claim the PDF is self-contained. Font embedding stabilizes PDF display but does not control editable DOCX/PPTX rendering on another device.
4. After any content, font, or layout correction, save the editable source again and re-export the PDF. The final preview and final export must come from that same revision.

## Compare the final preview and export

Render every exported PDF page/slide to images and compare with the final editable-source preview. Check an overview for page/slide count, order, pagination, whitespace and broad hierarchy, then inspect each page/slide at readable size for font substitution, line wrapping, spacing, alignment, bullet/symbol glyphs, clipping, overlap, image crops, chart labels and protected letterhead. Ensure no content is missing or duplicated. Correct material mismatches in the editable source and repeat the export and comparison. If preview images are unavailable, inspect the editable source and PDF renders independently and state that a direct comparison was not possible.

## Grayscale checks

Theme 1 requires a grayscale proof for every dual-use artifact. Also run grayscale proofing for an explicit grayscale/print request and for printed circulation or handouts where the selected theme requires it. Inspect the rendered proof at the intended page or handout size; color-only distinctions, faint rules and small labels must remain understandable. A digital grayscale proof does not verify a physical printer. Preserve scientifically meaningful color keys and report when grayscale would destroy the intended evidence.

## Limits and honest reporting

The preview service, Word/PowerPoint, other office suites, operating systems, PDF viewers and printers can use different layout engines, fonts, versions, hinting and line-breaking rules. Exact pixel parity, identical pagination on every platform, or identical physical print output cannot be promised. A PDF fixes the appearance generated at export and embedded fonts reduce substitution risk; neither makes the editable source render identically everywhere.

Report the actual resolved font families and fallbacks, export workflow, whether PDF font embedding was verified, whether each-page visual comparison and required grayscale proof passed, and any unavailable checks. Do not claim a font was embedded or two outputs matched unless directly verified.
