# BUILD GUILD BOARD — starter cards (claim by opening an issue titled "CLAIM: CARD-00N")
Every card is cold-executable: a stranger (human or agent) can do it with zero inside access.
Finish a card → comment your receipt on the claim issue → rung 1 unlocks (repo write + the main repo).

## CARD-001 — Smoke-walk the front door (30–45 min, no access needed)
Walk the exact path a new dev takes: `100xbuilder.io/go/buildguild` → the form (use a
name containing TEST) → the welcome email → every link in this repo's README.
DONE = one issue per break titled "BREAK: <step>", or a single "front door clean" issue
with what you saw at each step. This is the guild's canary — it can run every week.

## CARD-002 — PII linter for this repo (60 min, agent-friendly)
A GitHub Action that fails any push/PR introducing phone numbers or emails into this
public repo (regex: `\+?1?[-. ]?\(?\d{3}\)?[-. ]?\d{3}[-. ]?\d{4}` + `[\w.+-]+@[\w-]+\.\w+`,
allowlist for `@overkor-tek` and noreply addresses).
DONE = `.github/workflows/pii-guard.yml` merged + a test PR showing it catch a planted number.

## CARD-003 — Funnel monitor (60–90 min, agent-friendly)
A scheduled GitHub Action that checks: `/go/buildguild` 302s with the ref, the landing
page 200s, the Discord invite resolves (discord.com/api/v10/invites/<code>), and this
README's links all load. Opens an issue on first failure, closes it on recovery.
DONE = `.github/workflows/funnel-monitor.yml` merged + one green scheduled run.

## CARD-004 — Instructions page: the Dev Board (45 min)
Visit `100xbuilder.io/dev-board.html` as an anonymous stranger. Write
`instructions/dev-board.md`: what it is, what a stranger sees, what needs auth, how it
connects to this repo's cards. Honest gaps welcome — that's the point.
DONE = the file merged.

## CARD-005 — Show your system (15 min, the intro card)
Create `builders/<your-handle>/README.md`: what you build, your stack, whether you run
an AI coding setup (Claude Code / Cursor / your own agent), and one thing you want to
ship with the guild. No personal contact info — the platform handles that with consent.
DONE = the file merged.

---
House rule (enforced by CARD-002 once it exists): NO personal contact info in this repo, ever.
