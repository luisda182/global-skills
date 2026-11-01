# Optional Lovable implementation handoff

Read when the brand project targets Lovable (including the spelling "Loveable"). Offer this group during scope definition; include it only when selected. Keep the skill business-neutral and use the project's approved identity.

## Scope and deliverables

List the selected handoff files and acceptance checks in the Gate A inventory. After Gate A, deliver `README-Lovable-<brand>.md` and `<brand>-app-kit.zip`, using the project's brand identifier. Include only selected, supported assets:
- A portable `public/` tree: SVG/ICO/PNG favicons, Apple touch icon, PWA any/maskable icons, social-sharing image, web manifest, and light/dark/mono logo variants in `public/brand/`. Record dimensions, safe zones and filenames.
- Brand CSS/JSON tokens and integration appropriate to the actual Vite/Tailwind/shadcn or other project setup. Inspect project versions when available; do not assume a particular Tailwind configuration format. For a reference-only handoff, state version assumptions.
- A reusable React logo component when React is used, supplied as a real source file alongside the guide.
- Metadata additions, font-loading guidance, placement examples, a concise Lovable implementation prompt, and a verification checklist.

## Integration rules

- Merge brand metadata into the existing HTML head. Preserve application scripts, required tags and unrelated integrations; update matching tags without duplication. Never direct Lovable to replace the entire head.
- Use inline SVG for a monochrome logo that inherits `currentColor`. An external SVG loaded through an `img` does not inherit the host page's color. External images must use explicit color variants. Preserve accessible naming and the canonical approved geometry.
- Use approved tokens and typography. Confirm web embedding/distribution rights before bundling fonts; installed desktop fonts are not evidence of web rights. Document legitimate loading methods, dependencies and reviewed fallbacks.
- Dark logo variants do not establish a full dark UI theme. Include dark mode only if designed and reviewed. Likewise, additional status colors and component rules require explicit design rather than copying a reference brand.
- Ask for the real domain when needed, or clearly mark it unresolved. Social image metadata needs the correct deployed absolute URL. Do not fabricate domains, claims or deployment results.
- Keep the application logic intact unless implementation changes were separately requested. The handoff is not a functioning app or permission to publish.

## Validation and portability

Check every documented file exists, archive paths resolve, SVGs render, raster dimensions/transparency match the inventory, manifest references resolve, and configuration matches its declared environment. Include dependencies locally where permitted; identify any external dependencies rather than shipping unexplained tool-runtime or blob links.

Distinguish packaged-file checks from browser, deployed social-preview, installation and device tests. Do not mark the latter passed without running them. Final assets still require Gate B.
