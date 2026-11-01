# Validation example: multiplayer party card game

Example only. Mode A; planning validation, no game implementation. Research date: 2026-11-01, Asia/Taipei.

## Brief and research

Assume private adult friend groups, 3–8 players, mobile browsers, one region, original family-friendly prompt/answer deck initially. No public matchmaking, chat, paid packs or child-targeted service. Confirm intended age/content policy before development.

[Cards Against Humanity](https://www.cardsagainsthumanity.com/) provides the prompt-and-answer category reference. [Quiplash](https://www.jackboxgames.com/games/quiplash) is an adjacent prompt-response/voting comparator; [Jackbox joining](https://www.jackboxgames.com/how-to-play) informs browser/room-code entry. This project proposes a rotating judge, rather than assuming all competitor mechanics. Use original or explicitly licensed content; no competitor card text copied.

Differentiation hypothesis: quick private setup with clear recovery when a friend disconnects. Validate setup time and a full round with two friend groups; results pending. Reconnection and authority requirements derive from shared-state risk, not claims about competitor internals.

## Benchmark v1

Equal weights. Critical *. Capability anchors are cumulative 1 / 2 / 3 / 4 / 5.

| ID | Workflow | Capability anchors 1 → 5 | Proposed level-4 checks |
| --- | --- | --- | --- |
| G1 | Lobby | mock / create and join / capacity and host start / expiring code, reconnect identity and abuse limits / validated spectator support | 3–8 players; full/expired rooms rejected; brute-force join limited; host-only start |
| G2* | Private hands | sample cards / deal / draw and discard / server-held shuffled deck and recipient-only hand / validated configurable decks | Other hands and future deck absent from every client payload/log; forged card ownership rejected |
| G3* | Round submission | static / submit / collect and reveal / one accepted submission per player/round with stale-action rejection / validated multi-card variants | Duplicate, reordered, late and concurrent actions cause one legal effect; judge cannot submit |
| G4* | Judging/scoring | mock score / select winner / rotate judge / authoritative winner, single award and consistent next round / optional tested alternate rules | Two judge devices/racing requests award one point; nonjudge denied; replay does not rescore |
| G5* | Recovery | refresh demo / reconnect / resume own hand / server snapshot/version recovery, host loss and timeout policy / multi-region resilience if needed | Rejoin within proposed 60s restores own state; lost host does not freeze indefinitely; server restart test follows declared persistence policy |
| G6 | Content/access | sample text / readable cards / host content selection and removal / keyboard/touch flows, content labels, remove/rejoin prevention / user-tested advanced accessibility | Kicked token denied; malicious deck text rendered safely; named controls, focus, mobile layout |

Assurance levels: 1 demo; 2 repeatable simple checks; 3 automated core-state/permission checks; 4 adversarial concurrency, recovery, hidden-data, regression and operations evidence above; 5 sustained operations and additional independent validation appropriate to the service.

New product: all implementation absent, capability below level 1 (arithmetic 0), assurance U. Capability coverage 100%, bounds 0–0; assurance coverage 0%, bounds 0–5. No maturity attainment.

## State and architecture

State: lobby → dealing → submitting → judging → scoring → next round or finished. Disconnected is player connectivity, not permission to invent a second identity. Decide timeout, abandoned round, judge departure and deck exhaustion behavior explicitly.

Use a single authoritative room coordinator with versioned commands and durable snapshots if restart recovery is promised. A familiar backend with transactions/conditional writes may suffice; do not introduce a message bus or microservices for eight players. Browser clients send intentions, never authoritative score or hand assignments.

Command identity binds session, room, round, operation, target and payload. State/version guards and atomic deduplication protect replay. Recipient-specific views exclude hidden information. Telemetry records action metadata without logging hands/tokens.

Proposed performance budget: 100 concurrent eight-player rooms in one region, p95 accepted action broadcast under 500ms in the chosen test environment. This is a planning assumption, not observed capacity. Define load generation, network conditions and resource budget before approving it.

## Roadmap and batch G-01 v1

1. G-01: pure round engine with authority, hand projection, state transitions and score invariants.
2. G-02: lobby, room code/session identity and network commands.
3. G-03: reconnection, timeout/host-loss policy, persistence/recovery.
4. G-04: original deck, moderation/accessibility, load and operational evidence.

G-01 components: state reducer/coordinator, command schema, per-player projection and repository-native tests. No UI, scheduler, dependency or migration needed for this first pure-engine slice; persistence integration remains later and unverified. Before → after: given authorized players and a deck, one full round produces exactly one winner and legal next state.

Tests: all legal transitions, wrong actor, hidden projection, forged/unowned cards, duplicate requests, same key/different target, reordered and stale phase, racing awards, no duplicate card ownership, deck exhaustion and property-based/randomized legal sequences if supported. Do not mistake sequential reducer tests for network concurrency proof; integration races remain required in G-02/G-03.

Rollback: do not connect the new engine to live rooms until integration gates pass; preserve old engine behind configuration if one exists. G2 pending. No code changes, PR or deployment performed.

