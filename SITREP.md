# SITREP — ČS Dating Wien · Edícia I

**Last updated:** 2026-05-12 20:07
**Status:** SHIPPABLE — page + form live, blocked only by venue confirmation
**Edícia I:** Monday, 22 June 2026, 19:30–21:30, Wien 1. okres (venue TBD)
**Capacity:** 20 (10 M + 10 F) · **Price:** €69 → €39 (first edition discount)

---

## What's live right now

| Surface | URL | State |
|---|---|---|
| Public landing SK | https://jakub-ai23.github.io/cs-dating-wien/ | ✅ Live |
| Public landing CZ | https://jakub-ai23.github.io/cs-dating-wien/index-cz.html | ✅ Live |
| Public landing EN | https://jakub-ai23.github.io/cs-dating-wien/index-en.html | ✅ Live |
| Registration form (Jotform) | https://pci.jotform.com/form/261314058164048 | ✅ Live, Stripe connected |
| Local preview server | http://localhost:8765/ | ✅ Running |

**Repo:** `jakub-ai23/cs-dating-wien` (private) on GitHub. Pages auto-deploys from `main`.

## Funnel state

```
Landing page → "Prihlásiť sa" CTA
   ↓
Jotform application (13 questions, ~3 min)
   ↓
LinkedIn or Instagram + identity verification
   ↓
Stripe payment €39 (or MORAVA = €0 for friends)
   ↓
Auto-email #1: "Tvoja prihláška dorazila..." [DRAFTED, not yet pasted into Jotform Notifier]
   ↓
[Manual review by Jakub + Martina within 24h]
   ↓
Email #2 — Accept (with venue) OR Reject + refund [DRAFTED]
```

## Hard blockers

1. **🔴 VENUE NOT CONFIRMED.** Cannot send Email #2 without address. 5 outreach drafts staged in Gmail (3 verified emails, 2 best-guess). Next move: send + follow up by phone.
2. **🟡 DNS to csdating.eu.** Domain purchase + DNS setup at GoDaddy pending. Once done, Pages CNAME + repo settings + hard-coded URL update.
3. **🟡 Stripe live test.** End-to-end €0.50 submission to verify webhook + email firing — not yet done.
4. **🟡 Jotform Notifier email.** Auto-confirmation HTML drafted but not yet pasted into Jotform Settings → Emails → Notifier.
5. **🟢 Jotform Trust Block.** Stripe-protected trust paragraph drafted, ready to paste; Stripe logo upload as separate Image element.

## Today's commits (latest 3 on `main`)

- `aeba7e5` — Favicon, Jotform PCI URL, scarcity 19/20, remove orphan upcoming-card
- `dc91a09` — Translate CZ and EN landing pages to match current SK source
- `2504419` — ČS Dating Edícia I: copy refinement, fabrication scrub, Jotform integration

## Open files / artifacts in `~/Projects/cs-dating-wien/`

- `SITREP.md` ← you are here
- `index.html` / `index-cz.html` / `index-en.html` (authoritative pages)
- `cz-sk-vienna/` (mirror folder, same content)
- `jotform-trust-block.html` — Stripe-protected trust paragraph for paste
- `jotform-custom.css` — burgundy theme override for Jotform Designer
- `jotform-email-confirmation.md` — Email #1 (auto-confirm)
- `jotform-email-acceptance.md` — Email #2 (manual send after approve)
- `images/favicon.svg` (+ 16/32/192 PNG, apple-touch-icon, .ico)
- `images/founder-martina.jpg`
- `images/stripe-logo.svg|png`
- `images/logo-static-union.svg|png` (clean logo for Jotform header)

## Gmail drafts (15 total — clean up needed)

✅ **Keep — 5 final German drafts** (no em/en dashes, no GitHub URL, phone +43 664 1386498):
- Rosewood Vienna → `vienna.events@rosewoodhotels.com`
- Hoxton / Cayo Coco → `hallo.cayococorooftop@thehox.com` (CC main hotel)
- Sophie 7 → `leitung@sophie7.at`
- Zeitgeist Vienna → `info@zeitgeist-vienna.com` (call to verify)
- Meliá Vienna / Altia Skybar → `melia.vienna@melia.com` (call to verify)

❌ **Delete — 10 obsolete drafts:**
- 5 English versions (first attempt)
- 5 German with em/en dashes + GitHub URL (second attempt)

## Domains (planned)

| Domain | Status | Purpose |
|---|---|---|
| `csdating.eu` | Buying via GoDaddy | Primary URL |
| `slavicdating.eu` | Buying via GoDaddy | Defensive parking (€7/yr), future Slavic expansion |
| `cs-dating.wien` | Considered, lower priority | Original plan, now superseded |

## Decisions on record

- **Language:** Slovak primary, Czech + English mirrors maintained in lockstep
- **Voice:** "vyberáme / prísny výber" — banned word `kuratovaný` permanently retired
- **Capacity:** 20 only (10+10), no overbooking, no waitlist for Edícia I
- **Refund:** Full refund within 72h if vetted-out OR if unhappy within 30 min on-site
- **Friends:** Use MORAVA code at checkout = free; same form, same data quality
- **Workflow automation:** NOT building Jotform Workflows for Edícia I (manual review, 20 entries = ~20 min total)
- **External Apple Pay path:** Not building for Edícia I (Stripe Link enabled = 1-click for returning users is enough)
- **Upcoming events grid:** Hidden until Edícia II date locked

## Next session — start here

1. Check Gmail for venue replies. Follow up phone calls for the 2 best-guess emails.
2. If a venue says yes → lock Email #2's `[VENUE NAME] / [ADRESA] / [U-Bahn info]` placeholders → open public outreach.
3. Once `csdating.eu` is in your hands → say "wire the domain" and Claude does the rest.
4. Paste the trust block + email #1 into Jotform Notifier (5 min).
5. €0.50 test Stripe transaction.

## North-star check

Edícia I is a P0 financial-gate-feeding mission. Filed under [REAL TEAM / Future Roundnet] expansion or stand-alone, depending on entity structure. Today's net minutes of work: significant — track on debrief.

— Zoya / Jocko, 2026-05-12 20:07
