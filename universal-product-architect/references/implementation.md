# Controlled development

Enter only with a valid G2 record covering the concrete plan. Support the complete approved scope; do not stop at screens or skeletons.

## Before editing

Read applicable repository instructions, conventions, dependency and lock files, CI, and deployment rules. Inspect current revision and worktree status. Record pre-existing changes and baseline failures; preserve them. Use the approved checkout/worktree policy. Do not reset, overwrite, reformat unrelated files, or expose secrets. If mutation is forbidden, stay read-only and prepare artifacts outside the repository.

Inspect scripts before running them: a test/build/install may modify tracked files, contact live services, or execute package hooks. Prefer isolated nonproduction fixtures. Package installation and infrastructure access must fit current permissions.

## Execute the approved slice

Implement UI, authoritative behavior, storage, integrations/executors, error and recovery paths together where needed. Use repository-native patterns and testing tools. Introduce a dependency or architecture change only when its benefit justifies the operational cost and it fits approval.

For migrations, document compatibility, old/new application overlap, backfill, validation, deployment order, and rollback or forward recovery. “IF NOT EXISTS” alone does not make a migration correct or safe. Rehearse consequential data changes on authorized disposable data. Never silently run production migrations.

Keep repeatable regression checks in the existing test/CI system where approved. Add targeted tests that verify behavior and risks; do not duplicate implementation details or introduce a universal test framework. For a small visual change, inspection and relevant existing checks may be enough.

## Verification and recovery

Run focused checks first, then relevant regression/build and risk checks from the plan. Diagnose failures; distinguish pre-existing from introduced with evidence, not assumption. Fix within scope and rerun impacted checks. Do not weaken tests, skip flaky security checks, or remove requirements to make the report green.

If a check cannot run, record the exact blocker and leave the criterion unverified. Stop retries that need new access, cost, risk, or scope; propose a concrete recovery. Do not claim CI passed from a local run.

Inspect the final diff for unexpected files, secrets, permissions, schema and compatibility effects. Prepare the evidence report and benchmark delta. A local draft PR description is reviewable preparation; creating/updating a remote PR needs authorization for that action. Release/deploy only under its own valid gate.

