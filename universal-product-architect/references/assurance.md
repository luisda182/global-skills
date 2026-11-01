# Architecture, risk, and verification

## Model the actual domain

Identify actors, assets, trust boundaries, allowed state transitions, invariants, retries, concurrency, external effects, deletion/retention, and abuse. Examples: club membership and spoiler visibility; round submission and judging; task editing and local persistence. A financial document lifecycle is one domain model, not a universal lifecycle.

Select the smallest architecture that meets constraints. Compare reuse of the existing design, a simpler alternative, and any proposed new component by delivery cost, operations, scale, integrity, and migration risk. A small local app may need no server or account system. A multiplayer app needs an authoritative coordinator for shared state; browser UI state cannot authorize actions or protect hidden hands.

## Risk selection

Classify by credible impact, exposure, reversibility, and data sensitivity; use the highest applicable profile and add mixed-risk checks. Record the rationale and excluded checks. Reassess when scope changes.

| Profile | Required evidence appropriate to the touched behavior |
| --- | --- |
| Visual, low impact | Relevant build/static checks, responsive and keyboard/focus inspection, contrast and accessible naming; use the repository's supported browsers |
| Ordinary feature | Boundary cases, focused unit/integration checks, main flow and a failure path, build, relevant regression |
| Shared or multiplayer state | Simultaneous actors, duplicate/reordered/stale requests, phase authority, hidden-data filtering, disconnect/rejoin, timeout/host loss, capacity/load targets |
| Identity/private data | Server authorization where a server exists, cross-account/tenant/object denial, privilege escalation, session expiry/revocation, input/output handling and sensitive logging checks |
| Money/irreversible effects | Atomicity or documented compensations, scoped idempotency, same key/different request rejection, reconciliation, authorization, fault injection, auditable recovery |
| Regulated/high consequence | Current authoritative rules, expert validation where required, traceable controls; no compliance claim from generic tests |

Security fundamentals apply to relevant surfaces: validate untrusted input at authority boundaries; output-encode; keep secrets out of clients and logs; minimize data; constrain privileges; review exposed dependencies and abuse/rate limits. Do not manufacture a tenant test for a single-user offline app, or skip object isolation in a private club because it lacks payments.

## Secure operations without a fixed stack

For shared controlled writes: authenticate actor; derive authority from trusted resources; authorize object and action; validate state/version and input; serialize or atomically guard conflicting effects; persist the result; record relevant events; return only permitted data. Choose database transactions, conditional writes, actors, or another proven mechanism supported by the stack.

Idempotency identity must bind actor/tenant as appropriate, operation, target, and canonical request content. Protect key reservation and effect atomically against different-target as well as same-target races. A prior result may be returned only after current authorization and without leaking another actor's result. Do not copy the ERP SQL template as verified code.

External effects need a durable intent/outbox or equivalent, idempotent dispatch, receipt tracking, retry bounds, reconciliation, and an operator recovery path. Never assert exactly-once delivery to an uncontrolled provider. Jobs need an actual scheduler/executor, retry policy, visibility, and failure handling; otherwise mark them incomplete or disabled.

## Level-4 operations

Define availability/latency budgets, capacity, observability, alerts, incident ownership, retention, backup/restore and recovery objectives only where applicable. Demonstrate recovery in an authorized nonproduction environment. Use an observation window justified by risk; ERP's 14-night rule is not a universal duration. No production history available means operational evidence remains pending. Security findings with material impact block readiness until closed or scope explicitly changed without hiding the risk.

