# Validation example: book club reading app

This is one application of the method, not the skill's scope. Mode A. Draft plan only; no app built. Research date: 2026-11-01, Asia/Taipei.

## Brief and research

Assume private adult clubs of 5–50 readers using mobile web, with volunteer organizers. Outcome hypothesis: members coordinate a shared read without scattered messages or accidental spoilers. Validate with five organizers before expanding scope. Exclude ebook sales, licensed ebook ingestion, payments, AI recommendations, and public discovery.

[Fable rooms](https://help.fable.co/article/88-what-are-rooms) organize discussion by reading section. [Bookclubs polls](https://help.bookclubs.com/support/solutions/articles/39000026568-how-to-create-a-poll) support choosing books and meeting times. These are observations; enforced spoiler visibility and privacy below are proposed requirements. Bookclubs setup and poll help disagree on tier access, so no tier claim enters this benchmark.

Differentiation hypothesis: a simple private club with reader-controlled spoiler boundaries and accessible meeting coordination. Test organizer setup completion and whether members understand preview visibility. No demand or usability result claimed.

## Benchmark v1

All weights 1. Critical items marked *. Each sequence is cumulative capability levels 1 / 2 / 3 / 4 / 5. Level-4 testable thresholds are proposed, to confirm before implementation.

| ID | Workflow | Capability anchors 1 → 5 | Level-4 verification |
| --- | --- | --- | --- |
| B1* | Membership/privacy | mock club / join club / organizer-managed private membership / revocable invites and removal enforced on all reads/writes / delegated administration | Two clubs cannot read each other's content; revoked/removed member denied on next request; expired/reused invite rejected |
| B2 | Shared reading | mock shelf / select title / schedule checkpoints and track progress / edit schedule without losing discussion links / optional multiple concurrent reads | Two device sessions converge after edit; page/chapter inputs bounded; edition mismatch explained |
| B3* | Spoiler-aware discussion | sample thread / post comment / section threads and hide/reveal / previews and notifications honor chosen boundary / user-tested advanced discussion tools | Hidden body absent from list/notification payload until reveal; access policy applies to deep links; sanitized output |
| B4 | Polls/meetings | mock meeting / create meeting / vote and RSVP / authoritative close time, one current vote per member and timezone display / calendar integrations | Duplicate vote changes do not inflate totals; close-time boundary; Asia/Taipei and US DST display cases |
| B5 | Notifications | sample reminder / manual send / scheduled opt-in reminder / retries, deduplication and delivery status / user-controlled advanced schedules | Executor runs; retry creates one visible reminder per event/member; revoked membership and opt-out checked at send |
| B6* | Moderation/usable access | sample UI / basic controls / report and organizer removal / keyboard-complete core flows, responsive layout, rate limits and reporting recovery / validated enhancements | Member cannot use organizer action; report review flow works; keyboard and screen-reader inspection |

Assurance anchors per row: 1 recorded demo; 2 repeatable happy-path check; 3 relevant automated integration and negative checks; 4 listed checks plus relevant regression, recovery and operational evidence; 5 sustained results and independent review justified by exposure. This does not impose a particular framework.

Current implementation: absent (new product) for all six; capability observed contribution 0, below level 1; assurance U for all. Capability coverage 100%, bounds 0–0; assurance coverage 0%, bounds 0–5. Neither target attained. A plan does not raise scores.

## Architecture and risks

Propose the team's familiar web stack, managed storage and server authorization if no stack is supplied. Select vendors after access/cost constraints are known. Data: clubs, memberships, reads/checkpoints, discussions, polls, votes, meetings, delivery intents. Authority derives club access from membership. No SQL RPC requirement; use the stack's supported atomic operations.

Risks: private-content leakage (high), spoiler leaks (medium), duplicate votes/reminders (medium), timezone confusion (medium), harassment (medium). Keep full text out of spoiler-sensitive payloads and sensitive logs. Discuss retention, deletion and member export behavior before implementation.

## Roadmap and approval-ready batch B-01 v1

1. B-01: club creation, revocable invitation, join/remove and isolated club read. Advances B1; prerequisite for all shared flows.
2. B-02: select reading, checkpoints and spoiler-aware discussions; B2/B3/B6.
3. B-03: polls, timezone-aware meetings and real notification executor; B4/B5.
4. B-04: capacity, usability, recovery and operational observation; reassess both lenses.

B-01 before → after: a user can create a club, invite another user and revoke their access. Components: membership UI, server membership/invite handlers, persistent membership store, authorization middleware, integration tests. Contract: pending invite → redeemed or revoked/expired; active member → removed. Server derives club scope; invite redemption is atomic and rate-limited.

Use additive schema if an existing stack is chosen; no deletion/backfill proposed. Tests: creator flow, wrong-club denial, expired/reused invite, concurrent redemption, removal followed by direct request, error/focus states, relevant build/regression. Rollback: disable invitations; retain memberships; revert compatible app version. No new third-party dependency justified yet. No scheduled job in this batch. Record actual stack and exact files before G2 approval.

G2 pending. No repository or deployment effects authorized. Batch done requires actual passing evidence, not this design review.

