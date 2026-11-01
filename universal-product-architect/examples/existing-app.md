# Validation example: existing app audit

Mode B → proposed Mode C. Read-only public source audit plus isolated execution probes. The app is TodoMVC JavaScript ES5 at revision ff43b02e59dfa604386bb382034b2cd07c2bcd8a. This is not an audit of the user's private app.

## Scope and inventory

Source: [app spec](https://github.com/tastejs/todomvc/blob/ff43b02e59dfa604386bb382034b2cd07c2bcd8a/app-spec.md), [store](https://github.com/tastejs/todomvc/blob/ff43b02e59dfa604386bb382034b2cd07c2bcd8a/examples/javascript-es5/src/store.js), model, controller, example package and test guide. Exact files and blob IDs are in review/fixtures/provenance.json; copied files retain MIT license.

Existing design: browser controller/model/store; no backend inspected or needed for this narrow local demo. Package lists build/dev scripts. Test guide describes Cypress and known legacy bootstrap issues; no CI pass inferred. Repository instructions outside fetched files were not fully audited; that inspection remains a prerequisite before any approved implementation.

Comparator scan: Todoist recurrence and Microsoft To Do dates are adjacent expectations for broader task managers, but are unnecessary to repair TodoMVC's published contract. Keep recurrence, cloud sync, accounts and payments out of scope.

## Benchmark v1 and findings

Equal weights, persistence critical. Proposed category is a reliable single-device task demo; no claim to full commercial task-manager parity.

| ID | Criterion and level-4 acceptance | Implementation | Capability / assurance |
| --- | --- | --- | --- |
| E1 | Add/edit/toggle/delete with trim, blank handling and correct counts | Source-present; some model behavior probed | U / U at whole-criterion scope; controller/DOM not run |
| E2 | All/active/completed routes and correct filtered updates | Controller source-present | U / U; browser not run |
| E3* | Tasks survive fresh page context using localStorage; edits persist; corrupt/unavailable storage handled | Memory-only store observed; fresh-context probe demonstrates loss | Capability 0 below level 1 for persistence / assurance U |
| E4 | Keyboard-accessible, responsive and safely rendered core flow | Not inspected fully | U / U |
| E5 | Repeatable regression and understandable recovery from storage errors | Test documentation exists; storage recovery absent in inspected store | U / U |

For E1/E2: level 1 mock, 2 happy path, 3 complete core behavior, 4 boundary/recovery plus usability, 5 validated advanced workflow. E3: level 1 persistence prototype, 2 basic persistence, 3 edit/delete persistence, 4 malformed/denied storage recovery, 5 validated import/export; this row's score 0 evaluates the required persistence behavior specifically, not the existence of memory CRUD. E4/E5: 1 ad hoc, 2 basic, 3 repeatable core coverage, 4 documented supported-environment checks and recovery, 5 sustained broader evidence.

Capability assessed coverage 20%, known weighted sum 0; lower/upper bounds 0–4; assessed mean 0 below level 1 over E3 alone. Assurance coverage 0%, bounds 0–5. Whole-product maturity is unknown; critical E3 failure blocks level 4 even though upper bound is 4. No numeric capability inferred merely from implemented-looking code.

FIND-E1: store uses closure memory, so data does not survive a fresh JavaScript context. This conflicts with the app spec's persistence requirement. It may be intentional for benchmark performance; maintainer intent requires confirmation. Do not silently change benchmark semantics.
FIND-E2: no storage-error recovery in the inspected store. This matters only if persistence is authorized.
FIND-E3: public test guide reports legacy initialization issues. Treat as documentation, not reproduced failures in this review.

See review/probe-results.json for actual isolated probe outcomes. A fresh VM context models module lifecycle, not a real browser reload. Browser, build and CI checks were not run.

## Proposed repair batch E-01 v1 (approval pending)

Before → after: local tasks currently disappear across contexts; after approval, persisted tasks reload with stable IDs and recoverable storage errors. Confirm whether a production persistence variant or benchmark memory variant is desired before G2.

Components: store adapter; initialization/error UI via existing app/view integration; focused storage tests and existing Cypress persistence flow. Inspect app/view/build and repository policies before final exact-file plan approval. Keep the existing JavaScript design. No new dependency, server, identity, RPC, ledger, or tenant layer.

Data contract: versioned stored collection, validated task fields and stable unique IDs; startup reads once, saves after mutations; don't overwrite malformed records automatically. Storage unavailable: explain volatile session mode and its limits. Preserve corrupt raw data for explicit recovery/export with consent; avoid logging task text.

Required checks: create then fresh context, edit/toggle/delete then fresh context, duplicate-title unique IDs, malformed JSON/schema, denied/quota storage, empty list, focused controller regression, actual browser reload/filter/keyboard flow, existing build and repository-native Cypress run. Confirm multi-tab behavior and either handle conflicts or explicitly document a single-tab limitation before level 4.

Rollout/recovery: versioned key, preserve prior data, rehearse compatibility; keep a backup before format upgrade. Disable persistence feature if initialization fails without deleting stored tasks. Any code/CI change or remote PR requires separate approval here.

## Local PR proposal (not created)

Title: Add an explicit persistent-storage variant for the JavaScript task demo

Body: The current memory store loses tasks when the application context is recreated, whereas the published app specification requires persistence. Subject to confirming benchmark intent, add a storage adapter with stable IDs and recoverable read/write errors while preserving existing controller/model behavior.

Validation to attach after implementation: targeted storage checks, browser persistence flow, relevant regression/build and failure recovery. This review contains no implementation or passing browser/CI claim.

Roadmap: confirm benchmark intent → approve exact E-01 → implement in authorized target → verify → reassess E1–E5. No repository, branch, commit, PR or deployment modified.

