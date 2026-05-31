# ČS Dating Wien — Project CLAUDE.md

**Created:** 2026-05-27
**Last updated:** 2026-05-27

Project config for Claude Code. This is the **authoritative** project file. The older `cz-sk-vienna/CLAUDE.md` is a legacy dev folder and is **stale** (€29 / 30 seats / "1. okres") — do not trust it for current state. Read `SITREP.md` + `STRATEGY.md` for live status before working.

---

## Project Identity

**ČS Dating Wien** — Česko-Slovenský Dating. Curated speed-dating evenings for Slovak and Czech people living in Vienna, ages 25–39. Serious partner search, not casual. Founded by Jakub Popluhar. Operations: Martina.

A **P0 financial-gate mission** (feeds the €10K/month north-star pillar). The product is shippable; the bottleneck is **distribution** (outreach + venue), not site quality.

**Edícia I:** Monday **22 June 2026**, 19:30–21:30, Wien · mystery venue (revealed 48h before to confirmed guests).
**Capacity:** 20 (10 men + 10 women).
**Pricing:** €69 standard. Code **EDITION1** (valid until 1 June 2026 00:00 CET) = −€30 + welcome drink → €39.

---

## Team

| Person | Role | Owns | Contact |
|---|---|---|---|
| **Jakub Popluhar** | Founder | Strategy, build, copy, site, analytics, impressum entity (private) | jakub@popluhar.at |
| **Martina** | Business partner · Operations (intended public lead) | FB/social marketing, community + event scouting, applicant social-proof vetting, on-the-ground promo | `[NEED FROM YOU: surname, email, phone]` |

- Both founders are **named and photographed** on the site (brand decision — no hiding behind a brand).
- Manual applicant review = **Jakub + Martina** jointly within 24h (see funnel in SITREP).
- **Role direction (from 29 May call):** Martina to become the public-facing lead/host; Jakub stays backstage as build/IT/automation + optional moderator. Not yet formalised.
- `[NEED FROM YOU / VERIFY]`: Martina's full name, contact, and exact split of operational ownership (who owns venue, who owns vetting). Contact kept in the **untracked** `outreach/` notes, never in this tracked file.
- Decisions are aligned with Martina before they ship. Log partner-level decisions in `SITREP.md` + the private `decisions.csv`.

---

## Live Surfaces

| Surface | URL |
|---|---|
| SK landing (primary) | `https://csdating.eu/` |
| CZ landing | `https://csdating.eu/cs/` |
| EN landing | `https://csdating.eu/en/` |
| Legal sets (×3 langs) | `/impressum/`, `/privacy-policy/`, `/terms/` (+ `/cs/…`, `/en/…`) |
| Application form | Jotform `261314058164048` (Stripe connected) |
| Analytics | 1×1 beacon on all 12 pages → `deflifeos.popluhar.at/t.gif?site=csdating` |

**Repo:** `jakub-ai23/cs-dating-wien` (public). GitHub Pages auto-deploys from `main`. HTTPS enforced, CNAME locked. **Push to `main` = live deploy** — preview before every push.

---

## Cloud Routines (scheduled remote agents)

This project runs scheduled remote agents on claude.ai. **Registry + full detail: `routines/README.md`.**
Manage at https://claude.ai/code/routines.

| Routine | Schedule | Mission |
|---|---|---|
| Outreach intel (`trig_01Bx1z7sihyxQiWbmrkCWg4T`) | daily 02:00 Europe/Vienna | Scan Gmail for replies to the community-outreach campaign, classify, auto-update `outreach/community-outreach.md` (its memory), and email Jakub a fire-ready follow-up. |

Key principle: a routine has **no cross-run memory** — the tracker file IS its memory. Don't break the
tracker's status column or the auto-push, or the routine starts double-reporting.

---

## File Map (root = authoritative)

```
cs-dating-wien/
├── CLAUDE.md            ← this file (authoritative)
├── SITREP.md            ← session handover / live status (read first)
├── STRATEGY.md          ← forward-looking decisions (edition evolution, no-photos pivot)
├── index.html           ← SK landing (primary)
├── cs/index.html        ← CZ landing
├── en/index.html        ← EN landing
├── {impressum,privacy-policy,terms}/  ← SK legal (+ cs/ + en/ mirrors)
├── images/              ← logos, founder photos, event photos, favicons
├── jotform-*.{css,md,html}  ← Jotform notifier emails + trust block + custom CSS
├── sitemap.xml, robots.txt, llms.txt, CNAME
└── cz-sk-vienna/        ← LEGACY dev folder — stale, ignore for state
```

---

## Brand Constants (do not change)

- **Full name:** Česko-Slovenský Dating (NOT "Československý")
- **Short mark:** ČS DATING
- **Colors (CSS vars in `index.html` `:root`):** `--burgundy #8b2252` · `--gold #b8912a` · `--ink #1a1208` · `--ivory #f8f4ee`. Logo language: SK = gold, CZ = burgundy.
- **Fonts:** Cormorant Garamond / Playfair Display (display), Inter (body)
- **Founders visible:** Jakub + Martina named and photographed. No hiding behind a brand.

---

## Social-Proof Seat Counter (editable)

Event card shows two gendered figure rows (men = gold silhouettes, women = burgundy). Counts are seeded social proof and **only ever go UP** (never decrement a public number).

- **Where:** `index.html` `<script>` IIFE — constants `MEN_TAKEN`, `WOMEN_TAKEN`, `PER_GENDER`. Mirror in `cs/index.html` + `en/index.html`.
- **Row labels:** `seat-row-label` markup near `id="seatGridMen"` / `id="seatGridWomen"`.
- **Rule:** keep the public number reconciled with real Jotform applications so it never has to drop. Bump as real sign-ups land.
- Current: 7 men / 6 women (set 2026-05-27).

---

## Positioning Principles (from STRATEGY.md)

- Quality over volume — 20 committed > 40 curious.
- No tire-kickers — refund only if organizer vets you out (full sum back within 72h). No 30-min on-site refund.
- Slovak-primary brand. CZ + EN are mirrors, not equal markets.
- Manual review of every applicant + LinkedIn/Instagram check.
- **Edition II differentiator:** "no photos" as a feature. Do NOT burn it early unless Edition I needs the no-photos pivot to fill (<60% capacity by T-10 days — see STRATEGY.md).

---

## Standing Rules (project-specific)

- **Three languages stay in sync.** Any content/social-proof/pricing change to `index.html` must be mirrored to `cs/index.html` + `en/index.html` (translated, not copied). A CZ visitor must never see different numbers than SK.
- **Mystery venue framing locked** everywhere — no "1. okres", no address until venue confirmed + Email #2 placeholders filled (`[VENUE NAME] / [ADRESA] / [U-Bahn info]`).
- **Impressum entity:** Jakub Popluhar private (Albertgasse 34/4, 1080 Wien). **NOT** REAL TEAM s.r.o.
- **Preview before deploy** (push = live). Headless screenshot or local preview first.
- **Copyright/voice:** SK copy follows the 9-movement reader journey in `cz-sk-vienna/cs-dating-briefing-final.md` (the copy brief is still valid even though that folder's CLAUDE.md is stale). No em/en dashes in German legal text.

---

## Key Decisions on Record

- **D-0245** Anchor pricing €69, code EDITION1 unlocks −€30 + welcome drink (until 1.6.)
- **D-0246** Impressum entity = Jakub Popluhar private, not REAL TEAM s.r.o.
- **D-0247** Edition II "no photos" differentiator; Edition I fallback contingency
- **D-0248** Cancellation: 7-day cutoff, no 30-min on-site refund
- **D-0249** Mystery venue framing locked

---

## Open Blockers (as of last SITREP 2026-05-17 — re-verify)

1. 🔴 **Venue not confirmed.** Mystery framing buys time; Email #2 can't send without a real address.
2. 🟡 **Distribution.** Outreach send + first paid sign-ups.
3. 🟢 **No-photos contingency** ready if <12 confirmed by T-10 days.
