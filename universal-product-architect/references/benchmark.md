# Capability and assurance benchmark

## Define before grading

Freeze a versioned scope, audience, comparison set, requirement IDs, level anchors, acceptance tests, critical flags, and optional weights before assessment. Changes need a reason and an impact note; never remove a failing criterion just to improve the score.

Use two lenses for each applicable requirement:
- **Capability:** what behavior exists and how complete it is.
- **Assurance:** how strongly behavior and controls are demonstrated.

Implementation state: absent / partial / implemented / unknown.
Verification state: not run / pass / fail / blocked / stale.
Keep these fields independent. “Not observed” is not “absent”; unknown is not zero maturity.

## Anchors

| Level | Capability | Assurance |
| --- | --- | --- |
| 1 | Demonstrable prototype of the workflow | Ad hoc demonstration with recorded limits |
| 2 | Basic usable happy path | Repeatable basic checks and input validation |
| 3 | Complete core workflow, useful errors and recovery | Relevant automated checks and essential trust controls demonstrated |
| 4 | Competitive, accessible, reliable category experience | Risk-selected automated regression, negative/failure checks, operational safeguards and recovery evidence |
| 5 | Demonstrated advanced value beyond level 4 | Sustained operational results plus deeper independent or adversarial validation where risk warrants |

For each requirement, replace broad anchors with cumulative, observable outcomes. Level 4 does not require every competitor feature. Establish latency, concurrency, accessibility, recovery, and observation-window thresholds before testing, grounded in intended users and risk. Proposed thresholds need confirmation before execution.

## Scores, uncertainty, and hard gates

Use equal weights unless impact justifies differences. Report the full matrix, denominator, weights, and assessed coverage. Score each lens 1–5 only where evidence supports an anchor; use U when unknown. Use 0 solely as a calculation placeholder for an observed absent required behavior, explicitly “below level 1,” never as a sixth maturity level.

For a lens with total applicable weight W, known weight K, and known weighted sum S:
- Assessed mean = S/K, or U if K=0.
- Coverage = K/W.
- Conservative whole-scope lower bound = S/W.
- Upper bound = (S + 5×(W−K))/W.

A lower bound treats unknown contribution as zero for arithmetic only; it does not assert absence. Do not present the assessed mean as whole-product maturity. Show unrounded numbers for threshold checks; display at most one decimal. N/A requires a scope rationale and is removed from W visibly. Deferred in-scope work stays in W.

Declare a lens ≥4 only when its lower bound ≥4, all critical items reach that lens's level-4 anchor, and no required check for the claim is failed, blocked, stale, or unrun. To declare the product at level 4, both lenses must qualify and all level-4 definition-of-done gates must pass. Noncritical items may be below 4 if the predeclared rubric allows that and all release requirements are met.

Retain the ERP guard: an implemented feature without passing relevant verification has a provisional capability ceiling of 3.5 and cannot satisfy a critical level-4 gate. Report its raw source-observed status separately; never invent a 3.5 score merely because code exists. Assurance remains U or the supported lower anchor. A failed security or integrity gate blocks level 4 regardless of weighted means.

## Tiny arithmetic example

Four equal-weight items, capability scores 4, 4, U, 2: assessed mean 3.33; coverage 75%; lower bound 2.50; upper bound 3.75. No level-4 claim. If all become 4 but a critical isolation check fails, capability behavior may be demonstrated, but assurance and product level 4 remain blocked.

