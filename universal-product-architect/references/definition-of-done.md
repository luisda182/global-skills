# Definition of done

Apply to a batch and separately to product maturity. A finished batch can leave the product below level 4.

## Batch completion

- Approved plan and authorization match delivered scope; material deviations resolved.
- All acceptance criteria delivered across UI, authority, persistence, executors/integrations and failures where relevant.
- Risk-selected checks actually pass on the delivered revision; failures, skips, blockers and pre-existing issues recorded.
- Relevant regression, build/static checks and UX/accessibility checks complete, or an explicit bounded limitation keeps affected claims unverified.
- Data compatibility and migration/recovery verified where affected.
- Evidence links each claim to criteria, revision, environment, command/procedure, expected and actual results.
- Benchmark and roadmap updated consistently; no source-only claim tagged VERIFIED.
- Release, operational and expert-review dependencies stated. No hidden production effects.

If required criteria or checks are outstanding, report “implemented, verification incomplete” or “partial,” not done. User acceptance of residual risk does not make a failed test pass.

## Product level 4

Both independent lenses meet the benchmark threshold and critical-item gates; coverage and bounds shown. Relevant authorization, privacy, integrity, accessibility, reliability, recovery, job execution, and operational controls are demonstrated against predeclared thresholds. No unresolved material release blocker. Expert/legal sign-off is present when applicable; otherwise do not claim compliance.

Do not require SSO, payroll, immutability, bilingual strings, SQL RLS, export watermarking, or a penetration test for every product. Introduce such requirements only from product needs and risk. Conversely, simplicity is not a reason to bypass security at actual trust boundaries.

## Report vocabulary

- Planned: specified only.
- Implemented: observed in source or delivered; not runtime proof.
- Verified: passing relevant checks at the identified revision and environment.
- Failed: observed mismatch; include reproduction and impact.
- Blocked / not run / stale: no current proof.
- Ready for review: draft artifacts complete; no implication of release readiness.

