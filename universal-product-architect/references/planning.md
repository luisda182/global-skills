# Plans and approval gates

Prepare a plan specific enough to approve without further invention. Link brief, research, benchmark version, criteria advanced and criteria at risk. Include behavior, components/files, state/API/data contracts, migrations, authorization, jobs, tests, rollout, rollback/recovery, dependencies, cost implications, out-of-scope items, and definition of done. Mark N/A with reasons.

## Gates

| Gate | Decision and record |
| --- | --- |
| G0: discovery | Scope and access: read-only investigation or artifact drafting within the user's request |
| G1: design baseline | Benchmark, trade-offs, assumptions, roadmap; obtain decisions that materially affect the batch |
| G2: implementation | Explicit approval of named plan version, scope, target repository/environment, and allowed code/data changes before editing |
| G3: external actions | Separate authorization for PR/branch writes, dependency installation if not already authorized, publishing/registration, deployment, or production data operations |
| G4: completion | Evidence review; remaining release blockers and residual risks visible |

Gate labels do not create approval requirements for harmless preparation beyond current authorization. Preserve prior valid approval; do not repeatedly ask for the same approved work. A request to plan or audit alone does not pass G2. Approval to implement does not automatically authorize deployment.

Use the authorization template to record approver/message, date, plan version, target, allowed effects, exclusions, and expiration conditions. No invented approval signatures. If a material deviation occurs, stop only affected work, present the revised plan and reason, and continue safe independent work.

## Batches

Prefer independently reviewable vertical slices. Order work by user value, risk reduction, dependencies, and effort. Avoid precise estimates without repository evidence. Each batch needs acceptance tests and recovery. Separate a data migration rehearsal from production execution. Explain irreversible migrations honestly; do not promise rollback that cannot restore deleted or transformed information.

When implementation is forbidden, deliver the complete plan, proposed test cases, draft PR title/body as a local artifact, and evidence gaps. Do not create a branch, commit, PR, or “temporary” repository modification.

