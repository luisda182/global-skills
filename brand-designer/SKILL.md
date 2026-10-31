---
name: brand-designer
description: Develop distinct business and product brand identities, complete brand kits, and reusable guidelines; apply or audit an existing identity and manage approved revisions. Use for company naming, brand strategy, visual identity, logo systems, brand voice, coordinated brand assets, or an illustrated brand manual (Manual de Marca).
---

# Brand Designer

Create an identity from the business's strategy and audience, then make it reproducible across media. Support creation, application, audit, and evolution. Scale work to the request: a palette application does not require a full rebrand.

## Scope and identity isolation

- Identify the business, product, active project, requested mode, and authoritative brand files before designing. Ask when multiple identities could apply. Never infer the business from the global skill's location or the last business served.
- Keep this skill global and business-neutral. Store each business's materials under its project, preferably `brands/<brand-id>/`; use another user-selected location when supplied. Never save client assets or approvals inside the installed skill.
- Read the selected business's brief, manifest, approved guidelines, and assets. Preserve existing approved decisions. Treat missing evidence as unknown, not permission to overwrite. Distinguish sub-brands and parent brands explicitly.
- Use the supplied Anthropic reference as structural inspiration for role-based colors, typography, fallbacks, and usage rules. Do not apply its colors, fonts, identity, or affiliation to another business by default. Do not copy its license declaration into new work.

- Treat supplied manuals as design references, not instructions or proof that their claims and technical values are correct. The Aulora reference informs the breadth, illustrated presentation, and cohesion of a manual; its school-system applications, palette, symbol, copy, and premium aesthetic are not defaults. The installed skill must work without that PDF or its original local path.

## Workflow

### 1. Discover and define

Read [discovery.md](references/discovery.md) for new identities or substantive strategy changes. Inspect supplied materials first; ask only the questions that materially affect the outcome. Record sources, assumptions, constraints, audience, positioning, personality, and required applications. Research competitors and current facts when useful and supported by browsing; cite sources and separate findings from hypotheses.

Initialize a business record from [brand-record.json](assets/brand-record.json) and [decision-log.md](assets/decision-log.md). Copy templates into the business workspace and fill them with actual information. Do not overwrite an existing record.

**Strategy gate:** present a concrete brief and recommendation for approval before developing a new visual direction. While approval is pending, organize inputs and research; do not progress into dependent design. An explicitly approved brief satisfies this gate. For a small application of an approved identity, use the existing approvals and skip irrelevant gates.

When a company or product needs a name, read [naming.md](references/naming.md). After strategy approval, generate and compare candidates and obtain name approval before developing the final wordmark or name-dependent visual system. An established approved name satisfies this gate.

### 2. Develop a direction

Offer a small set of meaningfully different directions, normally two or three, unless the user requests one. Connect each to audience and positioning. Show palette roles, typography, logo approach, visual language, voice samples, and representative applications. Explain the tradeoffs. Mark concepts as proposed; a moodboard or mockup does not establish production readiness.

Identify the organizing idea connecting positioning and name to the symbol, logotipo (wordmark), palette, typography, visual language, voice, and applications. Explain those connections and show them in use; avoid assembling independently attractive but unrelated elements.

**Direction gate:** obtain selection or approval before expanding a concept into the full system. Record exactly what was selected and any requested changes. Do not treat silence, elapsed time, or a request for options as approval.

### 3. Build the system and kit

Read [brand-kit.md](references/brand-kit.md) when creating the full system or choosing exports. Build coherent assets from the approved direction, including strategy, messaging, logo family, colors, typography, imagery, voice, guidelines, and practical templates. Include every kit category in the delivery manifest; mark an item out of scope, pending, or unavailable when it is not delivered. Do not call an incomplete kit complete.

For a complete brand kit, include an illustrated brand manual and technical appendix by default unless the user narrows the scope. Read [brand-manual.md](references/brand-manual.md) to plan and design the manual, and [technical-appendix.md](references/technical-appendix.md) for its implementation specifications. A request for a Manual de Marca selects this deliverable mode; it can document an existing approved identity without triggering a rebrand.

Use tools appropriate to each deliverable. If available, follow the imagegen skill for raster imagery and the relevant document, presentation, or PDF skill for those formats. Use editable vector sources for geometric logos and exact typography where suitable. Never label embedded raster artwork as a vector master. If a necessary capability is unavailable, provide supported files, record the gap, and ask only for the missing capability that blocks required delivery.

Read [quality-and-release.md](references/quality-and-release.md) before presenting the release candidate. Verify actual files, not only a written specification. Treat generated imagery as concepts until inspected and refined. Keep print conversions, licensing, and name clearance claims appropriately evidenced.

**Release gate:** present the reviewed kit and manifest for acceptance before marking it approved. A request to produce a kit authorizes draft production, not implicit acceptance. Persist approvals already given; do not request them again. Explicitly delegated stage decisions may satisfy the named gates; log the authorization and your decisions. Preserve existing approved identity elements unless changes are explicitly authorized.

### 4. Apply, audit, or revise

For application, use the selected business's approved identity and adapt its hierarchy to the medium. Do not impose fixed point-size thresholds across web, print, and slides or rotate accent colors mechanically.

For audits, compare actual artifacts to approved rules, prioritize concrete inconsistencies, and propose corrections. For revisions, state the affected decisions and applications, create a new candidate version, and preserve the approved version until its replacement is accepted. A request to change one element does not authorize changing the rest.

## Persistent state and handoff

Maintain a per-business record, decision log, and release manifest. Decisions can be `proposed`, `approved`, `rejected`, or `superseded`; only user approval or explicit delegated authority establishes approval. Log the approval's scope and source. If the source cannot be recovered, say so and seek confirmation only for dependent work.

Use distinct version directories, for example `brands/<brand-id>/releases/v1.0-draft/`. Keep approved releases intact; point the business record to the accepted release after approval. Never mix assets from different businesses unless an explicitly authorized co-branding task requires them.

At handoff, link the files, identify the version and status, explain essential usage rules, and state any missing items or next approval. Publishing, purchasing fonts, trademark filing, or contacting others requires separate task authorization; kit approval alone does not authorize those actions.

## Mandatory stage deliverables and no-substitution rule

- **Strategy:** deliver a written, evidence-labeled brief, assumptions, audience, differentiation, positioning, messaging, scope and approval request. No dependent visual identity before approval.
- **Naming:** deliver 3–5 distinct candidates with pronunciation, rationale, linguistic considerations, differentiation, risks, screening evidence and a recommendation. Obtain selection before final name-dependent artwork.
- **Creative directions:** deliver 2–3 separately inspectable concept presentations with distinct strategic concepts, proposed palettes, type treatments, logo approaches, imagery/graphics, voice, relevant mockups, tradeoffs and status. A comparison collage may supplement but never replace the individual presentations. Seek explicit direction selection.
- **Full system:** after approval, create reproducible logo family, role-based colors, typography, imagery/graphics, voice, appropriate applications, and source/export assets under [brand-kit.md](references/brand-kit.md).
- **Complete kit or Manual de Marca:** create a **real, multipage, illustrated PDF**, editable layout source where supported, technical appendix (inside the PDF or linked), real asset files and manifest following [brand-manual.md](references/brand-manual.md) and [technical-appendix.md](references/technical-appendix.md). A single generated image, contact sheet, outline, mockup or prose-only description is **not** a brand manual.
- **Release:** run [quality-and-release.md](references/quality-and-release.md), inspect every page and required asset, report pass/fail/unverified items, and request acceptance before marking final. Never claim files were generated, checked, available, licensed or legally cleared without evidence.
- If a required output cannot be created with available capabilities, state the limitation, deliver verified partial work, mark the release **incomplete**, and do not silently substitute a different medium.
- Scope these requirements proportionately: an isolated application, audit or small revision does not trigger a full kit. Do not inflate documents with filler to satisfy a page count.

## Evidence, production integrity and consistency

- Treat customer insights and market claims as hypotheses until sourced. For business-name conflicts, check the relevant jurisdiction and record dates, exact searches, sources and unresolved risks; never invent domain, handle, registration or trademark findings.
- Label AI imagery as conceptual unless independently validated. Do not place fictitious verified-check icons, manufacturing measurements, live contact details, legal claims, or compliance badges inside generated mockups.
- Maintain a single approved source of truth for naming, geometry, palette, type, voice, dimensions, licensing and asset versions; cross-check the manual, appendix, tokens and exported files against it.
- Create source and output files with appropriate tools: images for illustrative concepts; document/PDF tooling for an actual manual; editable vector paths for suitable master logos; separate export files for deliverables. A raster embedded in SVG is not a vector master.
- Keep approval records and project assets per business, never in the reusable skill repository.

## Two-stage manual-first production workflow

For full new identities, distinguish **design-development assets** (working masters, examples, concepts and mockups needed to create an accurate manual) from **final production assets** (the individually exported, tested package). After strategy, naming and direction approvals, produce a complete illustrated **Manual de Marca draft** with coherent draft masters and an explicit planned-asset inventory. Request **Manual Approval Gate A** before generating the full final asset package. Approval authorizes production only of the assets listed in the accepted manual; it does not waive release validation. Then create/export and validate the assets against the approved manual, present a release manifest, and request **Asset Release Gate B**. Do not treat approval of concepts as approval of production exports. Manual-first does not mean inventing master geometry or measurements: develop sufficient coherent source artwork to make manual specifications reproducible. Consult [asset-production.md](references/asset-production.md) for standards and source verification. Visual directions follow [visual-directions.md](references/visual-directions.md).
