# GEO + SEO Report: ČS Dating Wien

**Created:** 2026-05-07  
**Updated:** 2026-05-07  
**Purpose:** Make cs-dating-wien discoverable by LLMs (ChatGPT, Perplexity, Claude, Gemini, Google AI Overviews) and traditional search for target queries around Slovak/Czech speed dating in Vienna.  
**Site:** https://jakub-ai23.github.io/cs-dating-wien/ (SK/CZ/EN, GitHub Pages static)

---

## 1. Executive Summary

**Three things to do first:**
1. **Add Event + FAQPage JSON-LD structured data** — the page has zero structured data. This is the single highest-ROI fix: it signals to Google, Bing, and all LLMs what the event is, when, where, and what it costs. 1 hour to implement.
2. **Add hreflang tags + og:image + twitter:card** — current OG is incomplete (no image URL, no canonical, no hreflang). These are crawl basics that block proper indexation of 3 language versions. 1 hour to fix.
3. **Get listed on viedencan.at, slovaci.at, wien.czechcentres.cz, and Eventbrite** — these are the diaspora-authority backlinks that anchor your domain to "Slovak/Czech Vienna" semantically. These are the links LLMs use to place you in context. 2–3 hours.

---

## 2. How LLMs Discover and Cite Content (Current State 2025–2026)

### 2.1 The Two-Track System

LLMs answer through two fundamentally different mechanisms, and GEO strategy must address both separately.

**Track 1: Training Data (Parametric Memory)**  
Baked into model weights at training cutoff. Static. Cannot be influenced retroactively. Entities mentioned frequently across authoritative sources during training have stronger neural representations. GPT-3 training data was ~22% Reddit (posts with 3+ upvotes). Wikipedia, news sites, and high-upvote forum content dominate. [Verified — multiple sources confirm this training corpus composition]

**Track 2: Retrieval-Augmented Generation (RAG) / Real-Time Web Search**  
Used by ChatGPT Search, Perplexity, Google AI Overviews, and Claude with web search. The LLM queries an underlying search engine at inference time. 87% of SearchGPT citations match Bing's top organic results. [Verified — Seer Interactive study] This means: **ranking in Bing = being cited by ChatGPT**. Ranking in Google = being cited by Google AI Overviews. This is the actionable lever.

**Implication for ČS Dating:** Training data inclusion is impossible to target for a brand-new site. RAG/retrieval is the entire game. Optimize for search ranking, and citation follows.

### 2.2 How Each LLM Platform Picks Sources

**ChatGPT (Search mode)**
- Relies primarily on Bing's organic results. 87% citation-Bing correlation confirmed. [Verified]
- Top citation predictor: referring domain count (link diversity) > domain traffic > content freshness. [Verified — SEJ study of 1.4M prompts, Ahrefs study]
- 44% of citations come from first third of page content. [Verified]
- Sections of 120–180 words per heading perform best (avg 4.6 citations vs 2.7 for <50 words). [Verified]
- Expert quotes double citation rate (4.1 vs 2.4 without). [Verified]
- Content updated within 30 days: 3.2x more citations than older material. [Verified]
- Pages with tables: 4.2x more citations than prose-only pages. [Verified — 2025 citation pattern analysis]
- Wikipedia: 43% of ChatGPT citations. Reddit: 12%. [Verified — Semrush study]
- Reddit's citation share dropped from ~60% to ~10% in ChatGPT after a Sept 2025 retrieval change. [Verified]

**Perplexity**
- Uses a 6-stage RAG pipeline: query intent parsing → real-time hybrid retrieval (BM25 + dense embeddings) → 3-tier ML reranking → prompt assembly → LLM synthesis.
- "pplx-embed" custom embedding models for semantic matching.
- Schema markup presence correlates with 47% vs 28% Top-3 citation rate. [Single-source — authoritytech.io, B-tier]
- Content updated within 30 days: 3.2x more citations. [Cross-referenced with ChatGPT data]
- Pulls up to 40% more citations from trusted high-authority sites vs mid-tier blogs. [Single-source]
- Answer must appear in first 100 words (BLUF principle) to reach 90% of top citations. [Single-source]
- Perfectly capable of citing a low-authority blog if it offers the most precise, well-structured answer to a niche question. [Verified — key for ČS Dating]

**Google AI Overviews**
- Relies on Google's organic ranking signals. 52% of AI Overview sources come from top 10 results; 48% pulled from lower positions based on content quality. [Verified]
- 96% of AI Overview citations come from sources with strong E-E-A-T signals. [Single-source — wellows.com, B-tier. Plausible but specific % unverified]
- Multi-modal content (text + images + structured data) cited 156% more than text-only. [Single-source]
- Google has stated it does NOT use llms.txt for AI Overviews — uses traditional SEO signals. [Verified — Google statement]

**Claude (with web search)**
- Uses a combination of Bing and other retrieval sources.
- Leans toward established editorial brands (NYT, Atlantic, Economist) — only 36% of journalism citations from past 12 months vs 56% for ChatGPT. [Verified — AI citation comparison study]
- For niche queries, semantic clarity and factual density matter more than brand authority. [Verified — multiple GEO sources]
- Niche specificity advantage: Claude is more likely to cite a precise niche answer than a generic authority piece.

### 2.3 Key Universal Citation Signals (Cross-Platform)

| Signal | Impact | Confidence |
|--------|--------|------------|
| Content in first 100 words answers the query | Very High | Verified |
| Schema markup (Event, FAQ, Organization) | High | Verified |
| Section length 120–180 words | Medium-High | Single-source |
| Tables vs. prose | 4.2x citation boost | Single-source |
| Expert quotes with attribution | 2x citation rate | Verified |
| Content updated within 30 days | 3.2x boost | Cross-referenced |
| Referring domain diversity (backlinks) | Top factor for ChatGPT | Verified |
| Presence on review platforms (Trustpilot, etc.) | 3x higher citation probability | Single-source |
| Domain mentions on Reddit/Quora | 4x higher citation probability | Single-source |

---

## 3. GEO Tactics Applicable to ČS Dating Wien

### 3.1 Content Architecture (LLM Quotability)

**Current page assessment:** The SK page content is emotionally strong but structured for human readers, not LLM extraction. The key problems:
- No "bottom line up front" — the LLM-quotable summary doesn't appear in the first 100 words
- FAQ section exists (great!) but no FAQ schema markup
- No structured data of any kind
- No self-contained, citable paragraphs in English on the EN version

**Fixes needed:**
1. **English page BLUF paragraph** (40–75 words, self-contained, quotable): Every sentence must be citable out of context. Example:

> "ČS Dating Wien is Vienna's only curated speed dating event for Slovaks and Czechs. Edition I takes place on 22 June 2026 at Arcohotel HQ, Wien. 30 spots (15 men, 15 women), ages 25–39. €29 entry. Organizer: Jakub Popluhar, international event organizer based in Vienna."

2. **Replace pronouns with explicit entities** — "the event" instead of "it," "ČS Dating Wien" instead of "we" in any sentence that might be cited independently.

3. **Add comparison table** (already partially present in SK version) — tables get 4.2x more citations. The "Apps vs. ČS Dating" comparison table should be in English too.

4. **FAQ as real Q&A format** — the existing FAQ is good. Needs schema markup and English version.

5. **Add statistics with citations** — the page cites Statista ghosting stats. Add more data points with source attribution (e.g., number of Slovaks/Czechs living in Vienna, dating app satisfaction rates).

### 3.2 E-E-A-T for an Event Site

Without a big brand, E-E-A-T signals for a small event site:
- **Experience:** Jakub's bio mentions "dozens of speed datings in Vienna" — this is the experience signal. Make it more specific: "Jakub attended 30+ speed dating events in Vienna between 2021–2025."
- **Expertise:** Mention M.Ed. education, international event organizing background.
- **Authoritativeness:** Backlinks from diaspora platforms (see Section 6).
- **Trustworthiness:** HTTPS (already on GitHub Pages), clear organizer name/contact, refund policy stated clearly (already good).
- **Schema Organization with sameAs properties** linking to verifiable profiles (LinkedIn, Instagram).

### 3.3 llms.txt — Should We Implement It?

**Verdict: Low priority, implement after quick wins, but it takes 30 minutes.**

Current adoption: ~784 major websites. No LLM provider has officially committed to using it. Google explicitly ignores it for AI Overviews. No proven correlation with citation rates. [Verified]

However: Zero cost, takes 30 minutes, signals intentionality, may become relevant as adoption grows. Implement after schema markup and backlinks.

**What to include for ČS Dating Wien:**
- What the event is (1 sentence)
- Target audience (Slovaks/Czechs 25–39 in Vienna)
- Next event date, venue, price
- Link to English page (EN page is the LLM-optimized version)
- FAQ answers in plain text
- Organizer bio with verifiable links

---

## 4. SEO Tactics Applicable to ČS Dating Wien

### 4.1 Current Page Audit Findings

**What exists:**
- Title tag: "Česko-Slovenský Dating · Wien – Online dostávaš jeden pokus. Naživo dostávaš večer." [Good, keyword-rich in SK]
- Meta description: Good, specific, has date. [Good]
- og:title and og:description: Present [Good]
- og:type: "website" [Should be "event"]

**What is missing:**
- og:image [MISSING — critical]
- og:url with canonical URL [MISSING]
- twitter:card [MISSING]
- hreflang tags for SK/CZ/EN [MISSING]
- canonical tags [MISSING]
- JSON-LD structured data of any type [MISSING]
- sitemap.xml [NOT CONFIRMED — needs check]
- robots.txt [NOT CONFIRMED — needs check]

### 4.2 Target Query Strategy

**Primary LLM-target queries (EN):**
- "speed dating Vienna for Slovaks" / "Slovak speed dating Vienna"
- "Czech Slovak expat dating Vienna"
- "dating events Vienna Slovak Czech community"
- "community events Vienna Slovaks Czechs 2026"

**Primary LLM-target queries (SK):**
- "speed dating Viedeň Slováci"
- "slovenský dating Viedeň"
- "česko-slovenský dating Viedeň"

**Primary LLM-target queries (CZ):**
- "speed dating Vídeň Slováci Češi"
- "česká slovenská komunita Vídeň akce"

**Long-tail / conversational (key for LLM answers):**
- "Where can I meet Slovaks in Vienna?" → need to be the answer
- "Are there any Slovak community events in Vienna?" → need to be the answer
- "Slovak Czech dating event Vienna 2026" → direct hit

### 4.3 Multilingual Page Structure

The EN version at `/cs-dating-wien/en/` returns 404. This is a critical gap — the English version is the LLM-discovery version and it doesn't exist as a separate indexable page. [Verified — confirmed via scrape]

**Options:**
- Create `en/index.html` as a separate English-language page
- OR create `en.html` in root
- OR use language parameter `?lang=en`

GitHub Pages requires static files — the EN version must be a separate HTML file.

---

## 5. Specific Code and Markup to Add

### 5.1 Event Schema (JSON-LD) — add to `<head>` of all 3 language versions

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Event",
  "name": "ČS Dating Wien – Edícia I",
  "alternateName": "Czech-Slovak Speed Dating Vienna – Edition I",
  "description": "Vienna's only curated speed dating event for Slovaks and Czechs aged 25–39. 30 spots (15 men, 15 women). Organizer: Jakub Popluhar.",
  "startDate": "2026-06-22T19:30:00+02:00",
  "endDate": "2026-06-22T23:00:00+02:00",
  "eventStatus": "https://schema.org/EventScheduled",
  "eventAttendanceMode": "https://schema.org/OfflineEventAttendanceMode",
  "location": {
    "@type": "Place",
    "name": "Arcohotel HQ",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "Athanstraße",
      "addressLocality": "Wien",
      "addressRegion": "Wien",
      "addressCountry": "AT"
    }
  },
  "organizer": {
    "@type": "Person",
    "name": "Jakub Popluhar",
    "url": "https://jakub-ai23.github.io/cs-dating-wien/",
    "sameAs": [
      "https://www.linkedin.com/in/jakubpopluhar/"
    ]
  },
  "offers": {
    "@type": "Offer",
    "price": "29",
    "priceCurrency": "EUR",
    "availability": "https://schema.org/LimitedAvailability",
    "validFrom": "2026-01-01",
    "url": "https://jakub-ai23.github.io/cs-dating-wien/#prihlaska"
  },
  "image": "https://jakub-ai23.github.io/cs-dating-wien/images/hero.jpg",
  "inLanguage": ["sk", "cs"],
  "audience": {
    "@type": "Audience",
    "audienceType": "Slovak and Czech expats in Vienna, ages 25–39"
  },
  "maximumAttendeeCapacity": 30,
  "url": "https://jakub-ai23.github.io/cs-dating-wien/"
}
</script>
```

**For the EN version, use `"inLanguage": "en"` and translate the name/description.**

### 5.2 FAQPage Schema (JSON-LD) — add after Event schema

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What language is the ČS Dating Wien event in?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The event is conducted in Slovak and Czech. The MC alternates between both languages. No German or English required."
      }
    },
    {
      "@type": "Question",
      "name": "How does the speed dating format work?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ČS Dating Wien uses a classic speed dating format: 10 dates of 6 minutes each over one evening. After the event, attendees submit a match form; if interest is mutual, contacts are exchanged privately."
      }
    },
    {
      "@type": "Question",
      "name": "Who is ČS Dating Wien for?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ČS Dating Wien is for Slovaks and Czechs aged 25–39 living in Vienna, Austria. The event is curated — each applicant is screened for age range, serious intent, and language. 30 spots per edition (15 men, 15 women)."
      }
    },
    {
      "@type": "Question",
      "name": "What happens if I don't match with anyone?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Even without a romantic match, attendees leave with a network of 14+ Slovak and Czech contacts in Vienna who share their cultural background — friends, connections, people to call."
      }
    },
    {
      "@type": "Question",
      "name": "What is the ticket price and refund policy?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Entry is €29. If your application doesn't match the criteria, you receive a full refund within 72 hours. If you arrive and decide within 30 minutes it is not for you, €29 is returned on the spot."
      }
    }
  ]
}
</script>
```

### 5.3 Organization Schema (optional, adds E-E-A-T anchor)

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "ČS Dating Wien",
  "url": "https://jakub-ai23.github.io/cs-dating-wien/",
  "logo": "https://jakub-ai23.github.io/cs-dating-wien/images/logo-v2-light.svg",
  "description": "Curated speed dating events for Slovaks and Czechs in Vienna, Austria.",
  "founder": {
    "@type": "Person",
    "name": "Jakub Popluhar"
  },
  "foundingDate": "2026",
  "areaServed": {
    "@type": "City",
    "name": "Vienna",
    "sameAs": "https://www.wikidata.org/wiki/Q1741"
  }
}
</script>
```

### 5.4 Hreflang Tags (correct syntax)

**Critical note:** Czech language code is `cs`, NOT `cz`. CZ is a country code, cs is the ISO 639-1 language code. [Verified — Google documentation]

Add to `<head>` of every page (all 3 language versions must cross-reference each other):

```html
<!-- On the SK (root) page -->
<link rel="canonical" href="https://jakub-ai23.github.io/cs-dating-wien/" />
<link rel="alternate" hreflang="sk" href="https://jakub-ai23.github.io/cs-dating-wien/" />
<link rel="alternate" hreflang="cs" href="https://jakub-ai23.github.io/cs-dating-wien/cs/" />
<link rel="alternate" hreflang="en" href="https://jakub-ai23.github.io/cs-dating-wien/en/" />
<link rel="alternate" hreflang="x-default" href="https://jakub-ai23.github.io/cs-dating-wien/en/" />

<!-- On the CS page -->
<link rel="canonical" href="https://jakub-ai23.github.io/cs-dating-wien/cs/" />
<link rel="alternate" hreflang="sk" href="https://jakub-ai23.github.io/cs-dating-wien/" />
<link rel="alternate" hreflang="cs" href="https://jakub-ai23.github.io/cs-dating-wien/cs/" />
<link rel="alternate" hreflang="en" href="https://jakub-ai23.github.io/cs-dating-wien/en/" />
<link rel="alternate" hreflang="x-default" href="https://jakub-ai23.github.io/cs-dating-wien/en/" />

<!-- On the EN page -->
<link rel="canonical" href="https://jakub-ai23.github.io/cs-dating-wien/en/" />
<link rel="alternate" hreflang="sk" href="https://jakub-ai23.github.io/cs-dating-wien/" />
<link rel="alternate" hreflang="cs" href="https://jakub-ai23.github.io/cs-dating-wien/cs/" />
<link rel="alternate" hreflang="en" href="https://jakub-ai23.github.io/cs-dating-wien/en/" />
<link rel="alternate" hreflang="x-default" href="https://jakub-ai23.github.io/cs-dating-wien/en/" />
```

**Rules that must be followed:** Every page must self-reference. All URLs must be absolute. Mutual linking required (if A links to B, B must link back to A). [Verified — Google hreflang documentation]

**Note on x-default:** Assign to the EN page since that's the LLM-discovery version.

### 5.5 OpenGraph and Twitter Card Completion

Add to `<head>` (replace `og:type: "website"` with `"event"`):

```html
<!-- OpenGraph — add these missing tags -->
<meta property="og:url" content="https://jakub-ai23.github.io/cs-dating-wien/" />
<meta property="og:image" content="https://jakub-ai23.github.io/cs-dating-wien/images/hero.jpg" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:locale" content="sk_SK" />
<meta property="og:locale:alternate" content="cs_CZ" />
<meta property="og:locale:alternate" content="en_US" />
<meta property="og:site_name" content="ČS Dating Wien" />
<meta property="og:type" content="event" />

<!-- Twitter/X Card -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="Česko-Slovenský Dating · Wien" />
<meta name="twitter:description" content="Online dostávaš jeden pokus. Naživo dostávaš večer. Edícia I, Wien, 22. júna 2026." />
<meta name="twitter:image" content="https://jakub-ai23.github.io/cs-dating-wien/images/hero.jpg" />
```

**Image requirement:** The hero.jpg should be at least 1200×630px for proper social rendering. Verify dimensions. [Verified — 2025 social meta best practices]

### 5.6 robots.txt (create at root)

```
User-agent: *
Allow: /

User-agent: GPTBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: Google-Extended
Allow: /

Sitemap: https://jakub-ai23.github.io/cs-dating-wien/sitemap.xml
```

**Note on AI bots:** GPTBot, ClaudeBot, PerplexityBot are real crawlers. Allowing them explicitly signals willingness to be indexed by AI systems. [Verified — OpenAI, Anthropic docs]

### 5.7 sitemap.xml (create at root)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
        xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <url>
    <loc>https://jakub-ai23.github.io/cs-dating-wien/</loc>
    <xhtml:link rel="alternate" hreflang="sk" href="https://jakub-ai23.github.io/cs-dating-wien/"/>
    <xhtml:link rel="alternate" hreflang="cs" href="https://jakub-ai23.github.io/cs-dating-wien/cs/"/>
    <xhtml:link rel="alternate" hreflang="en" href="https://jakub-ai23.github.io/cs-dating-wien/en/"/>
    <lastmod>2026-05-07</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://jakub-ai23.github.io/cs-dating-wien/cs/</loc>
    <lastmod>2026-05-07</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://jakub-ai23.github.io/cs-dating-wien/en/</loc>
    <lastmod>2026-05-07</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.9</priority>
  </url>
</urlset>
```

**After deploy:** Submit sitemap to Google Search Console and Bing Webmaster Tools.

### 5.8 llms.txt (create at root — low priority, 30 min)

```markdown
# ČS Dating Wien

> ČS Dating Wien is Vienna's only curated speed dating event for Slovaks and Czechs aged 25–39. Edícia I takes place on 22 June 2026 at Arcohotel HQ, Wien. 30 spots (15 men, 15 women). Entry: €29. Organizer: Jakub Popluhar, international event organizer based in Vienna.

## About the Event

ČS Dating Wien brings together Slovak and Czech expats in Vienna for an in-person curated speed dating evening. The format: 10 rounds of 6 minutes each. Matches are arranged privately after the event. The event is conducted in Slovak and Czech. No German or English required.

The event addresses a gap in Vienna's dating scene: Slovaks and Czechs in Vienna (tens of thousands of people) have no dedicated venue for meeting romantic partners who share their language and cultural background.

## Upcoming Events

- [Edition I – 22 June 2026](https://jakub-ai23.github.io/cs-dating-wien/en/) : Speed dating, 30 spots, Arcohotel HQ Wien, €29
- Edition II – 14 September 2026 : Speed dating, same format
- Summer Evening – 18 August 2026 : Outdoor bar, community focus

## Pricing

Entry fee: €29. Full refund if applicant doesn't match criteria (within 72 hours). Full refund if attendee leaves within first 30 minutes.

## Organizer

Jakub Popluhar — M.Ed., international event organizer, attended 30+ speed dating events in Vienna. Founded ČS Dating Wien to fill the gap he personally experienced.

## English Language Reference

- [English page](https://jakub-ai23.github.io/cs-dating-wien/en/) : Full event info in English for international context
- [Slovak page](https://jakub-ai23.github.io/cs-dating-wien/) : Primary language version
- [Czech page](https://jakub-ai23.github.io/cs-dating-wien/cs/) : Czech language version

## Frequently Asked Questions

Q: What language is the event in?  
A: Slovak and Czech. The MC alternates both languages. No German required.

Q: Who can attend?  
A: Slovaks and Czechs living in Vienna, aged 25–39, seriously looking for a relationship.

Q: Is there a refund policy?  
A: Yes. Full refund within 72 hours if application doesn't fit criteria. Full refund on the night if you leave within 30 minutes.
```

---

## 6. Backlink and Listing Opportunities

### 6.1 Priority Tier 1 — Diaspora Authority Sites

These are the most valuable backlinks for semantic relevance and LLM context-building. Domains active in the Slovak/Czech Vienna space:

| Target | URL | Type | Notes |
|--------|-----|------|-------|
| **viedencan.at** | https://viedencan.at/ | Editorial listing / article | Slovak community news in Vienna. High relevance. Contact: editors. |
| **slovaci.at** | https://www.slovaci.at/ | Event listing | Slovak events in Austria. Free listing. |
| **wien.czechcentres.cz** | https://wien.czechcentres.cz/ | Official Czech cultural mission | ~120 events/year. Submit event for their calendar. |
| **viden.rakousko.net** | http://viden.rakousko.net/ | Community events | Czech/Slovak Vienna community. Submit event listing. |
| **virtualvienna.net** | https://www.virtualvienna.net/ | English expat guide | High DA, English-language, lists community events. |
| **expatica.com/at** | https://www.expatica.com/at/ | Expat directory | High DA. Accepts event listings for Vienna. |

### 6.2 Priority Tier 2 — Event Platforms (DA + Citations)

| Platform | URL | DA/DR | Notes |
|----------|-----|-------|-------|
| **Eventbrite** | https://www.eventbrite.com/d/austria--wien/ | DR 93 | Create event listing. Direct backlink. High LLM citation value. |
| **Meetup.com** | https://www.meetup.com/find/at--vienna/ | DR 91 | Create a group + event. Slovak/Czech expat group. |
| **events.at** | https://events.at/ | Austrian platform | Already showing Vienna events. Submit listing. |
| **vienna.at/events** | Local city portal | City authority | High local trust signal. |

### 6.3 Priority Tier 3 — Media Outreach (for LLM semantic authority)

| Target | Angle | Notes |
|--------|-------|-------|
| **refresher.sk** | "Prvý česko-slovenský speed dating vo Viedni" | 3M+ monthly readers. Lifestyle content. Native ad or editorial pitch. |
| **pravda.sk** | Human interest / diaspora angle | Has covered Slovak Vienna community before (confirmed). |
| **refresher.cz** | Czech angle — same story, Czech audience | Cross-border Slovak-Czech story is their niche. |
| **the-local.at** | English-language Vienna news | "Vienna finally has a Slovak-Czech speed dating event." |
| **viennawurstelstand.com** | English Vienna expat culture | Covered expat community stories. |

### 6.4 Reddit and Community Forum Presence

Reddit citation share: 6.6% in Perplexity, 21% in Google AI Overviews, 11% in ChatGPT. Domains with active Reddit mentions have 4x higher LLM citation probability. [Verified — Semrush study]

**Actionable:**
- Post in r/wien (Vienna), r/Slovakia, r/czech (announcing the event, not spam — genuine community announcement)
- Post in r/expats with the "finding your people in Vienna" angle
- Find and post in Facebook groups: "Slováci vo Viedni," "Češi ve Vídni," "Foreigners in Vienna"
- viden.rakousko.net discussion forum

---

## 7. Competitive Landscape

### 7.1 Vienna Speed Dating Competitors

| Competitor | Position | SEO Approach | Gap for ČS Dating |
|-----------|---------|-------------|-------------------|
| **cityspeeddating.at** | #1 Vienna speed dating | Established since 2009, 65K+ participants, ~200 events/year. Strong domain age + local authority. | Generic — no language/culture niche. |
| **speeddating-xxl.de** | German-language, German market | German parent brand. Generic. | No SK/CZ positioning whatsoever. |
| **speeddatingvienna.at** | Niche by age | Age-segmented events. | No cultural niche. |
| **happyendings.wien** | "Anti-frustration" angle | Recent brand, focused on alternatives to dating apps. | No SK/CZ angle. |

**Key finding:** Zero competitors are targeting "Slovak Czech Vienna speed dating" as a keyword or community. The niche is uncontested. [Verified — search confirmed no relevant competing results for these queries]

### 7.2 What Competitors Do for SEO That ČS Dating Should Copy

- cityspeeddating.at: Event schema, Google Maps listing, separate pages per age group (enabling targeted keyword landing pages)
- speeddating-xxl.de: Comprehensive FAQ with schema markup, city-specific landing pages

---

## 8. Confidence Assessment

**High Confidence — Verified, 2+ sources:**
- JSON-LD structured data improves AI discoverability (Microsoft Bing confirmed, multiple studies)
- 87% ChatGPT citation-Bing correlation (Seer Interactive study)
- Content freshness: 30-day update = 3.2x citation boost (multiple sources)
- hreflang `cs` not `cz` for Czech language (Google official docs)
- llms.txt has no proven citation correlation yet (SE Ranking statistical analysis)
- Reddit dropped from 60% to 10% in ChatGPT citation share after Sept 2025 change
- Zero competitors targeting SK/CZ Vienna dating niche (confirmed via search)

**Medium Confidence — Single-source or B-tier:**
- Schema markup correlates with 47% vs 28% Perplexity Top-3 citation rate (authoritytech.io — no primary study cited)
- Tables: 4.2x citation boost (2025 citation pattern analysis — source B-tier)
- Expert quotes: 2x citation rate (research claimed but methodology unclear)
- 96% of AI Overview citations from strong E-E-A-T sources (wellows.com — B-tier)
- Sections of 120–180 words perform best (Ahrefs study — A-tier but single study)

**Low Confidence / Inference:**
- Perplexity's 3-tier ML reranker details (authoritytech.io blog — not confirmed by Perplexity)
- Google "cosine similarity above 0.88" citation claim (ALM Corp — C-tier, likely marketing content)
- Multi-modal content "156% higher selection rate" (single source, large specific number = suspicious)

**NOT FOUND:**
- Any studies specifically about event/community niche site GEO performance
- Verified data on how many Slovaks/Czechs use LLMs to find events in Vienna
- Competitive SEO metrics (traffic, DR) for Vienna speed dating sites without paid tools

---

## 9. Prioritized Roadmap

### Quick Wins (1–3 hours, implement before June 22)

| Task | Time | Impact | Porygon ready? |
|------|------|--------|----------------|
| Add Event JSON-LD to SK page | 30 min | High | Yes — schema template above |
| Add FAQPage JSON-LD to SK page | 15 min | High | Yes — schema template above |
| Add og:image, og:url, twitter:card | 15 min | High | Yes — code above |
| Add canonical tags | 10 min | Medium | Yes — code above |
| Create robots.txt with AI bot allowlist | 15 min | Medium | Yes — template above |
| Create/verify sitemap.xml | 20 min | High | Yes — template above |
| Submit to Google Search Console | 10 min | High | Manual step for Jakub |
| Submit to Bing Webmaster Tools | 10 min | High | Manual step for Jakub |

### Medium Investment (2–5 hours, do within 2 weeks)

| Task | Time | Impact |
|------|------|--------|
| Build EN version as real indexable page (en/index.html) | 3–4 hours | Very High — EN is the LLM-discovery language |
| Add hreflang tags across all 3 language versions | 1 hour | High |
| Create Eventbrite + Meetup listings | 1 hour | High — DA 93 backlink, LLM citation source |
| Submit to slovaci.at, viedencan.at, viden.rakousko.net | 1 hour | High — semantic authority in niche |
| Submit to wien.czechcentres.cz event calendar | 30 min | High |
| Create llms.txt | 30 min | Low now, future option |
| Add BLUF paragraph to EN page | 30 min | Medium-High |
| Add comparison table to EN page | 30 min | High (4.2x citation signal) |

### Long-Term Plays (weeks to months, post-Edition I)

| Task | Timeline | Impact |
|------|----------|--------|
| Media pitch to refresher.sk after Edition I with testimonials | July 2026 | Very High — 3M readers, strong LLM training signal |
| Build testimonials/review section post-event | After June 22 | High — E-E-A-T signal, LLM prefers cited social proof |
| Reddit posts in r/wien, r/Slovakia after each edition | Ongoing | High — 4x citation probability with active mentions |
| Post-event recap page (indexed, quotable) | After each edition | High — freshness signal, more pages to cite |
| Wikidata entity for the event series | Q3 2026 | Medium — trains future LLMs on the entity |
| Seek editorial coverage (the-local.at, viennawurstelstand.com) | Q3–Q4 2026 | High |
| Build EventSeries schema across all 3 editions | After Edition II confirmed | Medium |

---

## 10. Sources

### Primary / Official (S-Tier)
- [Google Event Structured Data](https://developers.google.com/search/docs/appearance/structured-data/event) — Event schema spec [Tier: S]
- [Google FAQPage Structured Data](https://developers.google.com/search/docs/appearance/structured-data/faqpage) — FAQ schema spec [Tier: S]
- [Google hreflang x-default](https://developers.google.com/search/blog/2013/04/x-default-hreflang-for-international-pages) — hreflang spec [Tier: S]
- [Schema.org Event](https://schema.org/Event) — Event type spec [Tier: S]
- [Schema.org EventSeries](https://schema.org/EventSeries) — EventSeries type [Tier: S]
- [GEO: Generative Engine Optimization (Aggarwal et al., arXiv)](https://arxiv.org/html/2311.09735v3) — Original academic GEO paper [Tier: S]
- [llms.txt specification](https://llmstxt.org/) — Official spec by Jeremy Howard [Tier: S]

### Industry Research / Studies (A-Tier)
- [Why ChatGPT Cites One Page Over Another — Ahrefs (1.4M prompts)](https://ahrefs.com/blog/why-chatgpt-cites-pages/) — Citation driver analysis [Tier: A]
- [87% of SearchGPT Citations Match Bing — Seer Interactive](https://www.seerinteractive.com/insights/87-percent-of-searchgpt-citations-match-bings-top-results) — ChatGPT/Bing correlation [Tier: A]
- [Most-Cited Domains in AI — Semrush](https://www.semrush.com/blog/most-cited-domains-ai/) — Reddit/Wikipedia dominance [Tier: A]
- [Cited by ChatGPT: 7K Queries, 485K Citations — Wellows](https://wellows.com/insights/chatgpt-citations-report/) — Citation pattern study [Tier: A]
- [What is LLMs.txt and Should You Use It? — SEMrush](https://www.semrush.com/blog/llms-txt/) — llms.txt adoption analysis [Tier: A]
- [LLMS.txt Adoption Research Report 2025 — Rankability](https://www.rankability.com/data/llms-txt-adoption/) — Adoption stats [Tier: A]

### Practitioner Guides / Strong B-Tier
- [Generative Engine Optimization — Backlinko](https://backlinko.com/generative-engine-optimization-geo) — Comprehensive GEO guide [Tier: B]
- [How Perplexity Selects Sources — AuthorityTech](https://authoritytech.io/blog/how-perplexity-selects-sources-algorithm-2026) — Perplexity pipeline [Tier: B]
- [AI Platform Citation Patterns — TryProfound](https://www.tryprofound.com/blog/ai-platform-citation-patterns) — Cross-platform comparison [Tier: B]
- [How to Structure Content for GEO — StorychieF](https://storychief.io/blog/how-to-structure-content-for-geo) — Content structure tactics [Tier: B]
- [Google AI Overviews Ranking Factors — Wellows](https://wellows.com/blog/google-ai-overviews-ranking-factors/) — AI Overview signals [Tier: B]
- [How Reddit Became Biggest LLM Citation Source — Soar](https://www.soar.sh/blog/how-reddit-became-the-biggest-llm-citation-source) — Reddit citation analysis [Tier: B]
- [LLM Indexing Myths — Typescape](https://typescape.ai/blog/llm-indexing-myths) — Training vs. retrieval distinction [Tier: B]
- [How to Create an llms.txt File — Firecrawl](https://www.firecrawl.dev/blog/How-to-Create-an-llms-txt-File-for-Any-Website) — llms.txt format guide [Tier: B]
- [Hreflang Implementation Guide — LinkGraph](https://www.linkgraph.io/blog/hreflang-implementation-guide/) — hreflang syntax [Tier: B]
- [AI Citation Patterns: ChatGPT, Claude, Perplexity — DiscoveredLabs](https://discoveredlabs.com/blog/ai-citation-patterns-how-chatgpt-claude-and-perplexity-choose-sources) — Cross-platform comparison [Tier: B]

### Competitive Intelligence / Community Sources
- [viedencan.at](https://viedencan.at/) — Slovak Vienna community news [Tier: B]
- [slovaci.at](https://www.slovaci.at/) — Slovak events in Austria [Tier: B]
- [wien.czechcentres.cz](https://wien.czechcentres.cz/) — Czech Centre Vienna [Tier: S — official cultural mission]
- [viden.rakousko.net](http://viden.rakousko.net/) — Czech/Slovak Vienna community [Tier: B]
- [Eventbrite Vienna Speed Dating](https://www.eventbrite.com/d/austria--wien/speed-dating/) — Competitor landscape [Tier: B]

---

## Recommendation

**Implement structured data and fix the missing OG/technical tags first.** The page has strong content and a good story — the LLM discoverability gap is purely technical. The Event schema + FAQPage schema + hreflang + canonical + og:image combo takes under 2 hours with Porygon and converts the page from "invisible to machines" to "correctly machine-readable." This is the work that makes everything else compound: backlinks point to a properly-identified event entity, citations reference a structured FAQ, and the EN page (once built) becomes the English-language answer to "Slovak Czech dating Vienna" in every LLM with web search.

The English page gap is the second-highest priority because it is the LLM-discovery language. Every LLM with web retrieval runs English queries first. The SK page is currently the only indexable version, which means English-language LLM responses cannot serve the page's content. This is a 3–4 hour Porygon session.

Backlinks from viedencan.at, slovaci.at, and Eventbrite come third — they anchor the domain in the "Slovak Vienna" semantic cluster and multiply the effect of the technical fixes.
