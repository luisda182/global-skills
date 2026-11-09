# Cost and handoff

## Separate cost categories

- **Development and delivery:** Metered builders, paid services, infrastructure needed for verification, and expected rework. Prefer existing tools and a bounded batch when they meet the same requirements.
- **Assistant work:** Reuse approved scope and verified findings. Read the smallest relevant set of files. Batch independent lookups and run targeted checks before broader checks required by the risk or repository.
- **Product operation:** Choose a unit tied to the workflow, such as cost per completed job, active account, or tenant per month. Separate measured costs from estimates. Record volume, retries, failures, storage and external usage where relevant. Use N/A for absent categories and mark unknown inputs explicitly.

For products using metered inference, model a representative usage range and include failed calls and retries. Compare manual or deterministic paths, reuse of saved outputs, and justified model calls. Define an appropriate usage or cost guard and record how it will be measured. Apply the same principle to other metered services. Check provider pricing when it materially affects a decision.

## Resume from a short handoff

Record approved scope and effects, repository revision and environment, affected workflows, design reference if applicable, migration or rollout state, checks with outcomes, and unresolved decisions. Reuse valid evidence. Recheck items affected by changes in revision, environment, requirements, or risk. Keep the handoff in the existing plan or verification record.
