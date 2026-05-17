# ČS Dating Wien — Submission Battle Plan

**Created:** 2026-05-07
**Purpose:** Step-by-step manual submission guide for Jakub. Order matters. Total time: ~2 hours spread over 1–2 days.
**Live URL:** https://jakub-ai23.github.io/cs-dating-wien/

---

## PHASE 1 — Search Engine Indexing (do TODAY, ~30 min)

### 1.1 Google Search Console — submit sitemap
**URL:** https://search.google.com/search-console
**Why:** Tells Google your site exists and to crawl it. Without this, Google may not find your site for weeks. Without indexing, ChatGPT (which leans on Bing) AND Google AI Overviews can't cite you.

**Steps:**
1. Go to https://search.google.com/search-console
2. Click "Add property" → "URL prefix" → enter `https://jakub-ai23.github.io/cs-dating-wien/`
3. Verify ownership: easiest is "HTML tag" → copy the meta tag → tell me, I'll add it to the HTML and push → re-verify
4. Once verified: left sidebar → "Sitemaps" → enter `sitemap.xml` → Submit
5. Then: left sidebar → "URL Inspection" → paste each of the 3 URLs (root, /index-cz.html, /index-en.html) → click "Request Indexing" for each

**Expected:** Indexing 24h–7 days. Status will show "Submitted" then later "Discovered" then "Indexed".

---

### 1.2 Bing Webmaster Tools — submit sitemap
**URL:** https://www.bing.com/webmasters
**Why:** **CRITICAL.** 87% of ChatGPT citations come from Bing's top results. This is the #1 GEO action.

**Steps:**
1. Go to https://www.bing.com/webmasters
2. Sign in with Microsoft account (create one if needed)
3. Add site: `https://jakub-ai23.github.io/cs-dating-wien/`
4. **Shortcut:** import from Google Search Console if already verified there (saves 10 min)
5. Otherwise verify via meta tag (same process as Google)
6. Once verified: "Sitemaps" → submit `sitemap.xml`
7. "URL Submission" → submit all 3 URLs individually (Bing has fast indexing for new submissions)

**Expected:** Bing indexes faster than Google for small sites. Often within 24h.

---

## PHASE 2 — Event Listings (do this week, ~45 min)

### 2.1 Eventbrite — create event listing
**URL:** https://www.eventbrite.com/organizer/overview/
**Why:** DR 93 domain, ChatGPT cites Eventbrite frequently for event queries. Free for free or low-priced events.

**Steps:**
1. Sign up / log in at eventbrite.com
2. "Create event"
3. Fill in:
   - **Title:** ČS Dating Wien — Edícia I (Speed Dating for Slovaks & Czechs in Vienna)
   - **Date:** 22 June 2026, 19:30–21:30 (open end)
   - **Location:** Arcohotel HQ, Athanstraße, Wien
   - **Type:** Singles & Dating event
   - **Description:** Use the BLUF paragraph from `llms.txt` as the opening. Then describe the format (10 dates, 6 minutes each), add the matching mechanism, end with "More info: https://jakub-ai23.github.io/cs-dating-wien/"
   - **Image:** Upload `images/hero.jpg`
   - **Tickets:** €29 (use Eventbrite's payment processor OR mark as "External link" pointing to your Tally form once you have it)
4. Set to "Public"
5. Publish

**Expected:** Indexed by Google within 48h. Begins ranking for "speed dating Vienna" tail queries within 1–2 weeks.

---

### 2.2 Meetup.com — create group + event
**URL:** https://www.meetup.com/start/
**Why:** DR 91, strong community signals, indexed by ChatGPT and Google AI Overviews for "[city] events" queries.

**Steps:**
1. Sign up at meetup.com
2. **Create a group first** (events live inside groups):
   - Name: "Czech & Slovak Singles Vienna" or "ČS Dating Wien"
   - Topics: Singles, Dating, Czech, Slovak, Vienna
   - Description: 1–2 sentences pointing to the website
3. Create event inside the group with the same details as Eventbrite
4. Set to "Public" and "Visible in search"

**Cost:** Meetup charges ~€16/month for organizers. Worth it for 2–3 months around the event.

---

### 2.3 events.at — Austrian event listing
**URL:** https://events.at/
**Why:** Vienna-specific local SEO signal.

**Steps:**
1. Find their "submit event" form (usually footer)
2. Submit: title, date, venue, description, link

**Cost:** Free.

---

## PHASE 3 — Diaspora Authority Sites (do within 2 weeks, ~30 min)

These are the highest semantic value backlinks. Even one or two of these will significantly boost LLM citation probability for SK/CZ-specific queries.

### 3.1 Czech Centre Vienna (Czech Centres = Czech government cultural mission)
**URL:** https://wien.czechcentres.cz/
**Why:** Tier S — official Czech cultural institution. ~120 events/year on their calendar. High DA, trusted by LLMs.
**Action:** Find their event submission form OR email them directly.
**Email template (in Czech):**
```
Předmět: Návrh na zařazení do kalendáře akcí — Česko-slovenský speed dating ve Vídni

Dobrý den,

jsem Jakub Popluhar, organizátor nového kuratelovaného speed dating večera pro Čechy a Slováky ve Vídni. První edice se koná 22. června 2026 v Arcohotel HQ, 1. Distrikt.

Cílová skupina: Češi a Slováci 25–39 žijící ve Vídni. Kapacita 30 míst (15+15).

Více informací: https://jakub-ai23.github.io/cs-dating-wien/index-cz.html

Bylo by možné zařadit naši akci do vašeho kalendáře?

Děkuji,
Jakub Popluhar
```

### 3.2 slovaci.at — Slovak events in Austria
**URL:** https://www.slovaci.at/
**Why:** Dedicated Slovak community in Austria. High relevance, decent DA.
**Action:** Find submission form OR contact them via email/social.

### 3.3 viedencan.at — Slovak Vienna community news
**URL:** https://viedencan.at/
**Why:** Slovak-language Vienna news site. Could pitch as community story, not just listing.
**Action:** Editorial pitch (better than listing). Frame: "First Slovak-Czech speed dating event in Vienna." Use Slovak email template above.

### 3.4 viden.rakousko.net — Czech/Slovak Vienna community hub
**URL:** http://viden.rakousko.net/
**Why:** Active forum for Czechs and Slovaks in Vienna.
**Action:** Submit to event board AND post in their discussion forum about the event.

### 3.5 virtualvienna.net — English-language expat guide
**URL:** https://www.virtualvienna.net/
**Why:** High DA expat directory. Good for the EN page discoverability.
**Action:** Submit event listing in English.

### 3.6 expatica.com/at — High DA expat directory
**URL:** https://www.expatica.com/at/
**Why:** Major international expat platform. EN traffic.
**Action:** Find Vienna events submission OR pitch as community feature.

---

## PHASE 4 — Reddit + Forums (do close to event, ~30 min)

**Why:** Active Reddit mentions = 4x higher LLM citation probability. ChatGPT pulls Reddit threads frequently.

**Strategy:** Post 4–6 weeks before each event. Don't spam — one well-written post per subreddit.

### 4.1 r/wien
**Title (German):** "Neuer Speed-Dating Abend für Slowaken und Tschechen in Wien"
**Body:** Brief, transparent, link to the EN or DE version of the page.

### 4.2 r/Slovakia + r/czech
**Title:** "First curated Slovak/Czech speed dating in Vienna — Edition I, June 22"
**Body:** Diaspora angle. Link to SK/CZ versions respectively.

### 4.3 r/expats
**Title:** "Found my people in Vienna — Slovak/Czech community speed dating"
**Body:** Personal angle. Link to EN version.

### 4.4 Facebook groups
- "Slováci vo Viedni"
- "Češi ve Vídni"
- "Foreigners in Vienna"
- "Slovenská a česká komunita Viedeň"

Post once per group, 4 weeks before event.

---

## PHASE 5 — Post-Edícia I Media Push (after 22 June 2026)

This is where the real authority compound happens. After the first event runs successfully:

### 5.1 Editorial pitches
- **refresher.sk** — 3M+ monthly readers. Pitch with 1–2 participant quotes. Title: "Prvý česko-slovenský speed dating vo Viedni — ako to dopadlo."
- **the-local.at** — English Vienna news. Title: "Vienna's new niche dating event for Eastern European expats."
- **viennawurstelstand.com** — Vienna expat culture. Personal/community angle.
- **pravda.sk** — Slovak national daily. Has covered Vienna Slovak community before.

### 5.2 Post-event recap page
Create `/edicia-i-recap.html` with:
- 1–2 photos from the event
- 2–3 anonymized testimonials
- Numbers (X people came, X matches, X follow-up dates)
- This page becomes a fresh-signal cite for LLMs and Google

### 5.3 Wikidata entity (Q3 2026)
Once 2 editions have run, create a Wikidata entity for the event series. This is the single highest-leverage long-term GEO move — Wikidata is training data for almost every major LLM.

---

## CHECKLIST — Manual Tasks for Jakub

Copy this into your TODO and tick off as you go:

```
PHASE 1 (today, 30 min)
[ ] Google Search Console: verify property + submit sitemap.xml + request indexing on 3 URLs
[ ] Bing Webmaster Tools: verify (or import from GSC) + submit sitemap.xml + URL submission on 3 URLs

PHASE 2 (this week, 45 min)
[ ] Eventbrite: create event listing with hero.jpg + Tally link (once Tally exists)
[ ] Meetup: create "ČS Dating Wien" group + Edícia I event
[ ] events.at: submit event

PHASE 3 (within 2 weeks, 30 min)
[ ] Czech Centre Vienna: email pitch (Czech template above)
[ ] slovaci.at: submit listing
[ ] viedencan.at: editorial pitch
[ ] viden.rakousko.net: event board + forum post
[ ] virtualvienna.net: EN listing
[ ] expatica.com/at: EN listing

PHASE 4 (4 weeks before event, 30 min)
[ ] r/wien, r/Slovakia, r/czech, r/expats — one post each
[ ] Facebook groups (4 groups, one post each)

PHASE 5 (post-event, July 2026+)
[ ] refresher.sk pitch with testimonials
[ ] the-local.at pitch
[ ] viennawurstelstand.com pitch
[ ] Build /edicia-i-recap.html
[ ] Wikidata entity (Q3 2026)
```

---

## What's Already Done (Technical Layer)

✅ Event JSON-LD schema on all 3 pages
✅ FAQPage JSON-LD schema on all 3 pages
✅ Hreflang tags (SK/CZ/EN with x-default)
✅ Canonical tags on all 3 pages
✅ OpenGraph + Twitter Card metadata
✅ robots.txt with AI bot allowlist (GPTBot, PerplexityBot, ClaudeBot, Google-Extended)
✅ sitemap.xml with hreflang cross-references
✅ llms.txt for emerging LLM-friendly site descriptions

**Result:** The site is now machine-readable for ChatGPT, Claude, Perplexity, Google AI Overviews, and traditional search engines. The submissions above are what triggers actual indexing and citation.

---

## Time Investment Summary

| Phase | When | Time |
|---|---|---|
| 1. Search engine indexing | Today | 30 min |
| 2. Event listings | This week | 45 min |
| 3. Diaspora authority sites | Within 2 weeks | 30 min |
| 4. Reddit + forums | 4 weeks before each event | 30 min per event |
| 5. Post-event media | After Edícia I | 2–3 hours, spread |

**Total before launch:** ~2 hours of manual submissions across 1–2 weeks.
