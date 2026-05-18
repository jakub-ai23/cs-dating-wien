# SITREP — ČS Dating Wien · Edícia I — 2026-05-17

**Last updated:** 2026-05-17 17:57
**Status:** **LIVE.** Site shipped in 3 languages, all legal pages, analytics streaming. Blocked only on venue confirmation and outreach send.
**Edícia I:** Monday, 22. 6. 2026, 19:30–21:30, Wien (Mystery location)
**Capacity:** 20 (10 men + 10 women) · **Pricing:** €69 standard · code **EDITION1** until 1. 6. 2026 = −€30 + welcome drink → €39
**Live URL:** https://csdating.eu/

---

## What's live right now

| Surface | URL | State |
|---|---|---|
| SK landing | `https://csdating.eu/` | ✅ Live |
| CZ landing | `https://csdating.eu/cs/` | ✅ Live (clean URL, no `.html`) |
| EN landing (UK) | `https://csdating.eu/en/` | ✅ Live |
| SK legal set | `/impressum/`, `/privacy-policy/`, `/terms/` | ✅ Live |
| CZ legal set | `/cs/impressum/`, `/cs/privacy-policy/`, `/cs/terms/` | ✅ Live |
| EN legal set | `/en/impressum/`, `/en/privacy-policy/`, `/en/terms/` | ✅ Live |
| Jotform application | `https://pci.jotform.com/form/261314058164048` | ✅ Live (confirmed working by commander) |
| Stripe payment | Connected via Jotform | ✅ Live (confirmed working) |
| Analytics beacon | All 12 pages → `deflifeos.popluhar.at/t.gif?site=csdating` | ✅ Firing, logged to permanent CSV |

**Repo:** `jakub-ai23/cs-dating-wien` (public) on GitHub. Pages auto-deploys from `main`. HTTPS enforced. CNAME locked.

---

## Funnel state

```
csdating.eu/ (SK) | /cs/ (CZ) | /en/ (EN)
   ↓
"Prihlásiť sa" — top-right nav CTA goes to #termin (event card with seat grid)
   ↓
Section VI "Prečo my" — Why us section users naturally see during scroll
   ↓
Final CTA section #prihlaska
   ↓
Jotform application (13 questions, ~3 min) — code EDITION1 → −€30 + welcome drink
   ↓
LinkedIn / Instagram + identity verification
   ↓
Stripe payment €39 (with code) or €69 (without)
   ↓
Auto-email #1 confirmation (live)
   ↓
[Manual review by Jakub + Martina within 24h]
   ↓
Email #2 — Accept (venue revealed) OR Reject + 72h refund
```

---

## Pricing mechanic (anchor + claim, NOT anchor + drop)

- **Standard €69** dominantly displayed in hero pill and pricing card
- **Voucher code EDITION1** (typed at Jotform Stripe checkout) = −€30 + welcome drink
- Code expires **1. 6. 2026 00:00 CET**
- Welcome-drink endowment pill: typewriter + live countdown + depleting bar (window 2026-05-13 → 2026-06-01)
- After 1. 6. the pill auto-hides via JS and the CTA reverts to "Prihlásiť sa za €69"

**Refund language unified:** "plnú sumu späť do 72 hodín" if vetted out by organizer. NO 30-min on-site refund (removed — incentivises tire-kickers per commander).

---

## Blockers (hard / soft)

| # | Blocker | Plan |
|---|---|---|
| 🔴 1 | **Venue NOT confirmed.** Mystery framing buys time, but Email #2 can't go out without a real address. | Commander has appointments **next week** (after 2026-05-18). 5 outreach drafts staged in Gmail (Rosewood, Hoxton, Sophie 7, Zeitgeist, Meliá). |
| 🟡 2 | **No paid sign-ups yet.** Site live but not promoted. | Outreach phase starts next session. WhatsApp messages drafted in this session, ready to send. |
| 🟢 3 | **No-photos contingency.** Edition II differentiator can be pulled forward if Edition I stalls. | Captured in `STRATEGY.md`. Trigger: <12 confirmed seats by T-10 days. |

---

## What got built today (2026-05-17)

**Site (11 commits, `cad02d2` → `819f519`):**
- DNS wired csdating.eu via GoDaddy → GitHub Pages (typo + parking-record fixes)
- 3 SK legal pages drafted (private organizer, NOT REAL TEAM Sport s.r.o.)
- Pricing pivot to anchor+claim (3 iterations: strikethrough → both visible → code mechanic)
- Welcome-drink pill: typewriter + countdown + depleting bar + breathing wine emoji + shimmer
- 2 critic loops (27 + 4 issues found, all fixed)
- CZ + EN translation via 2 parallel translator agents with 2-pass internal QA + critic loop
- Clean URLs `/cs/`, `/en/` (folder/index.html pattern; old `index-cz.html` and `index-en.html` deprecated)
- Mystery-venue framing locked everywhere (no "1. okres")
- Analytics beacon on all 12 pages
- Top-right nav CTA routes to `#termin` so users pass through "Why us" before form

**Analytics retention system (commits in `~/Projects/ops`):**
- Permanent CSV archive on VPS at `/root/analytics/archive/<site>/YYYY-MM.csv`
- Privacy: IP + UA hashed with daily-stable salt, never raw
- Mac mirror at `~/Projects/analytics-archive/` (auto-pulled by `sync-vps.sh`)
- Hourly cron at `:05` past every hour
- Backfill mode for historical access-log recovery (`--from-access-log`)
- **955 rows backfilled**: csdating 10, futureroundnet 899, jakubpopluhar 46

**Internal artifacts:**
- `STRATEGY.md` — Edition II no-photos differentiator + Edition I fallback contingency
- Mission report: `~/Projects/ops/mission-reports/2026-05-17-cs-dating-wien-launch-sprint.md`
- Scene Protocol: `~/Projects/content/raw/2026-05-17-anchor-and-claim-vs-anchor-and-drop.md`
- TODO.md "Analytics Expansion (indexed, not revised)" section — 10 capability areas parked

---

## Next session — start here

**Read first:**
1. This SITREP
2. `~/.claude/projects/-Users-mr-magico/memory/hot.md` (current state cache)
3. Today's mission report addendum (analytics retention build)

**Top priorities (in order):**

1. **Venue follow-up.** Commander has appointments scheduled. After each, decide: lock venue, or escalate cold-call list. If a venue says yes → unlock Email #2's `[VENUE NAME] / [ADRESA] / [U-Bahn info]` placeholders.

2. **Outreach send.** WhatsApp messages drafted in this session (M / F / forwardable / "Hey...Attacke!" variant) — commander has them. Identify first ~20 personal contacts and start sending. Track sends + replies somewhere lightweight (a count in this SITREP works for Edition I).

3. **First sign-ups in the funnel.** Watch `~/Projects/analytics-archive/csdating/` for real visitor traffic + Jotform inbox for first applications. Use code `EDITION1` rate as the canary for whether the code mechanic is landing.

4. **Stripe coupon `EDITION1` verification** (one-time check). Commander already added the code in Jotform — verify a test transaction (€0.50) goes through at €39 with the code typed in. Should already be working per commander, but never tested end-to-end with a real card.

5. **Situation Room "Websites" panel** (P2 once parallel session lands). Per-site daily/weekly traffic, language split for csdating, switch behaviour. Parallel session owns `server.js` and `situation-room.html` — coordinate before touching.

6. **Analytics Expansion items** (indexed, pull when needed): UTM redirects on csdating.eu like `csdating.eu/ig` → IG attribution, conversion-event beacons on Jotform thank-you + Stripe success, Microsoft Clarity layer. Full list in `~/.claude/projects/-Users-mr-magico/memory/TODO.md` under "Analytics Expansion".

---

## Decisions on record (today)

- **D-0245** Anchor pricing at €69, code EDITION1 unlocks −€30 + welcome drink (until 1.6.)
- **D-0246** Impressum entity = Jakub Popluhar private (Albertgasse 34/4, 1080 Wien). NOT REAL TEAM s.r.o.
- **D-0247** Edition II no-photos as selling point; Edition I fallback contingency captured
- **D-0248** Cancellation policy: 7-day cutoff, no 30-min on-site refund
- **D-0249** Mystery venue framing locked (no "1. okres" anywhere)

---

## North-star check

Edícia I is a P0 financial-gate-feeding mission. Tonight the product is shippable in 3 languages with privacy-clean legal cover, working payment, permanent analytics. **The remaining gap is distribution.** Site quality is no longer the bottleneck. Outreach + venue is.

— Zoya / Jocko, 2026-05-17 17:57
