# DAEMON PROTOCOL — ČS Dating Wien Website Rebuild

Created: 2026-05-07
Status: **PHASE 2 — BRIEF · Awaiting GO**

---

## COMMANDER'S INTENT

Ship a landing page that makes a Slovak or Czech person in Vienna read it and think "shut up and take my money" by the time they hit the form. One evening. 30 people. Their language. No translation needed.

---

## PHASE 1 — PLAN

### End State (reverse-planned)

Both `index-v2.html` (dark) and `index-new.html` (light editorial) are production-ready with:
- Full copy rewrite per `cs-dating-briefing-final.md`
- V2 Pulse Union logo in nav of both files
- New "Skúšal/-a si to inak" section between hero and pyramid
- Authority strip under hero
- Gender-split pain section with correct voice
- Founders section (Jakub + Martina placeholder)
- Embedded signup form with Stripe placeholder
- Autonomy block before CTA

### Milestones (reverse order)

1. Both files open side by side, copy verified against 9-movement reader journey
2. Porygon completes `index-new.html` copy pass
3. CC completes `index-v2.html` copy pass
4. Both agents read: briefing + Hormozi + SURF + Slavic literature
5. GO signal received from commander

### PACE Plan

| Dependency | P | A | C | E |
|---|---|---|---|---|
| Slavic literature doc | `~/Projects/content/research/2026-04-20-E-slavic-literature.md` | Search `content/` for `slavic-literature.md` | Write female copy without it, flag for Martina | Leave female copy placeholder |
| Hormozi profile | `~/Projects/content/voice-library/alex-hormozi-voice-profile.md` | Already loaded in context | Use Hormozi rules from memory | Basic short-sentence copy |
| SURF method | `~/Projects/content/SURF-method.md` | Already loaded in context | Apply SURF rules from memory | Basic CTA copy |
| index-new.html (Porygon) | SendMessage to Porygon | New Agent spawn | CC does both files sequentially | CC does dark version only |

### Actions On

```
ACTION ON Slavic doc not found:     Write female draft, mark [MARTINA FINALIZES], continue
ACTION ON Porygon blocked:          CC does both files sequentially
ACTION ON copy rejected by Jakub:   Rewrite flagged section only, not full page
ACTION ON scope change mid-build:   Finish current section, checkpoint, then adapt
ACTION ON Tally URL still missing:  Keep placeholder, mark clearly in HTML comment
```

---

## PHASE 2 — BRIEF (SMEAC)

### ROSTER FOR THIS MISSION

| Agent | Pokémon | Role | Why |
|---|---|---|---|
| CC (main) | — | Rewrites `index-v2.html`, coordinates | Owns dark version |
| Porygon | Porygon | Rewrites `index-new.html` | Owns light version, runs parallel |

### SITUATION

Two website files exist. Design is done. Copy is weak — no story, no 9-movement reader journey. Full brief delivered in `cs-dating-briefing-final.md`. Logo V2 chosen (Pulse Union) but not yet in HTML files.

### MISSION

Rewrite all copy in both files per `cs-dating-briefing-final.md`. Embed V2 logo in both navs. No design changes. Both files ship production-ready on GO.

### EXECUTION

**CC — `index-v2.html` (dark):**
1. Read: `cs-dating-briefing-final.md` + Hormozi + SURF + Slavic literature doc
2. Replace nav logo with V2 Pulse Union SVG (inline)
3. Rewrite hero: new H1, authority strip, keep trilingual fade-in
4. Insert "Skúšal/-a si to inak" section after hero
5. Rewrite pain section (male: CC voice / female: Slavic substrate draft)
6. Rewrite pyramid intro + conclusion
7. Rewrite 4 difference cards
8. Tighten format section result lines
9. Rewrite founder bio with credentials
10. Update autonomy block per brief
11. Open file in browser

**Porygon — `index-new.html` (light):**
Same list. Receives full brief via SendMessage. Runs in parallel.

### ADMIN

- All files: `~/Projects/ops/cz-sk-vienna/`
- Brief: `cs-dating-briefing-final.md` (in same folder)
- Logo source: `logo.html` V2 section

### COMMS

Commander says GO → CC starts + briefs Porygon simultaneously → both deliver → commander reviews side by side.

---

## PHASE 3 — EXECUTE

**Status: WAITING FOR GO**

---

## PHASE 4 — DEBRIEF

*To be completed after execution.*

---

## PHASE 5 — LEARN

*To be completed after execution.*
