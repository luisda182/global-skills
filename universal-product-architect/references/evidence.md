# Evidence and audit records

Maintain one traceable chain: source claim → requirement → plan batch → implementation revision → check → result → maturity decision.

Use stable IDs: SRC-n, REQ-n, RISK-n, PLAN-n/version, TEST-n, EV-n, FIND-n. A record includes timestamp with timezone, owner/actor, source/revision or artifact hash, environment and versions, procedure/command, expected and actual results, exit status/counts, artifact path, scope limits and status. Record N/A with rationale. Redact tokens and personal data; use synthetic fixtures.

Store audit artifacts in the authorized location. In a repository only after approval, use its evidence conventions (for example docs/audit/batch-NN.md). Otherwise keep them in the review package. Record a commit only when one exists; never fabricate a SHA for uncommitted work. Hash a draft snapshot when useful.

Tags can be [IMPL], [VERIFIED: TEST-n @ revision], [PENDING], [FAILED: FIND-n]. Verification scope must be explicit: a source probe is not browser validation; provider documentation is not an independent product test; local tests are not CI; a simulated model is not a running application.

## Failed and stale evidence

Retain original failures and corrective reruns. A changed implementation, dependency, configuration, environment, or acceptance condition may invalidate prior checks; rerun affected checks. Do not erase history or average failures into passes. Report expected negative-test failures separately from failed checks.

## Coverage

For each criterion show required checks and pass/fail/skipped/not-run counts. No test files found is not evidence of no tests anywhere. A README claim about CI is source evidence only until the relevant run is inspected. A passing unit probe cannot establish end-to-end behavior, concurrency correctness, accessibility, or production reliability.

Use the verification template for summaries and a machine-readable log when it improves reproducibility. Keep findings and roadmap linked so known gaps do not vanish between batches.

