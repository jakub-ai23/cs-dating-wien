# SITREP — Česko-Slovenský Dating Wien

**Stand:** 2026-05-07, mid-day
**Branch:** `claude/review-vienna-report-Uvi1g`
**Letzter Commit vor diesem Sitrep:** `abaf4ed` (gender-split format section)
**Sprache:** SK only (CZ + EN parking lot until SK locked)

---

## TL;DR

V1 der Site komplett geschrieben in **zwei parallelen Voice-Versionen** (Original poetisch + Hormozi -30% direkt). Logo gewählt + integriert. Pyramide + Format-Sektion (gender-split) drin. **Flyer fehlt. Tally + Stripe nicht angeschlossen. Founder-Foto fehlt. Domain TBD.**

Insgesamt: **~75 % bereit für Soft-Launch.** Sieben Blockierer warten auf dich.

---

## STATUS — was steht definitiv

### Brand
- **Name:** Česko-Slovenský Dating (lang) / **ČS DATING** (Logo-Mark)
- **Logo:** V1 Binary Circles — zwei sich umkreisende Kreise (gold + burgundy), animiert 22s
- **Tagline:** "V tom istom jazyku. V tom istom kruhu."
- **Pre-Question Hook:** *"Sick of dating apps und having nothing in common?"* (German-English code-switch — pure Vienna-immigrant audience signature)

### Format
- 30 Plätze pro Abend (15 + 15)
- €29 / Person
- **22. Juni 2026** — Edícia I, Wien 1. Bezirk
- 3-4 Edícia / Jahr, max
- Founder hostet: **Jakub Popluhar**
- Operations: **Martina**

### Audience (Filter)
- SK + CZ in Wien, Alter 25-39
- Vorhaben: ernsthafte Partnersuche + Networking
- **NICHT** auf Beruf gefiltert — auf Sprache/Kultur/Intent

---

## DATEIEN IM REPO (`cz-sk-vienna/`)

| Datei | Inhalt | Status |
|-------|--------|--------|
| `index.html` | Original-Version (poetisch, premium-warm) | ✅ V1 fertig |
| `index-hormozi.html` | Hormozi -30% Version (direkter, harte Zahlen) | ✅ V1 fertig |
| `logo.html` | 3 Logo-Konzepte (V1/V2/V3) — V1 gewählt | ✅ Showcase bleibt |
| `briefing.md` | Positionierung, Brand-Optionen | ⚠️ leicht stale (Brand-Working-Title "Kruh" drin, kein Schaden, low priority) |
| `founder.jpg` | Founder-Foto | ❌ **FEHLT — du droppst rein** |
| `flyer.html` | Print-ready Flyer | ❌ **NICHT GEBAUT** |
| `SITREP.md` | dieses Dokument | ✅ |

---

## PREVIEW-URLS (sofort öffenbar — Mobile + Desktop)

- **Original:** https://htmlpreview.github.io/?https://github.com/jakub-ai23/ops/blob/claude/review-vienna-report-Uvi1g/cz-sk-vienna/index.html
- **Hormozi -30%:** https://htmlpreview.github.io/?https://github.com/jakub-ai23/ops/blob/claude/review-vienna-report-Uvi1g/cz-sk-vienna/index-hormozi.html
- **Logo-Showcase:** https://htmlpreview.github.io/?https://github.com/jakub-ai23/ops/blob/claude/review-vienna-report-Uvi1g/cz-sk-vienna/logo.html

> Caveat: Google Fonts laden manchmal nicht durch htmlpreview-Proxy → System-Fallback Serif/Sans. Layout, Farben, Animation arbeiten trotzdem. Auf lokalem `file://` öffnen ist garantiert sauber.

---

## SEKTIONEN AUF DER SITE (beide Versionen identisch strukturell)

1. **Nav** — animiertes V1 Logo + Apply-CTA
2. **Hero** — Pre-Question + H1 + Sub + Meta-Row + CTAs
3. **Pain** ("Poznáš to?") — Sprache als Intimitätsbarriere
4. **Pyramid of Long-Term Relationships** — Gottman + Perel als Quellen, 4 Ebenen foundation-up: Sprache/Kultur → Hodnoty/Viera/Rodina → Emotional Connection → Spoločný smer
5. **Difference** — 4 Cards: Apps · ČS Dating · Generic Events · Medzi svojimi
6. **Format** — Gender-split: Apps Pre muža (900 swipov) · Pre ženu (performance-flirteri) · alebo · Jeden večer s nami + Friendship-Bonus
7. **Founder** — Jakub-Bio + Operations Martina (Foto-Slot wartet auf `founder.jpg`)
8. **How It Works** — 3 Steps: Prihlás → Schvaľujeme → Príď
9. **Quote** — Placeholder-Testimonial (anpassen sobald echte da)
10. **Event Card** — Edícia I, 22. Juni 2026, prominentes Single-Event-Display
11. **FAQ** — 7 Fragen (Sprache, Anwesenheit, Prihláška, Networking, Preis, kein Match, ďalšie edície)
12. **Final CTA** — Tally-Link Placeholder (`tally.so/r/PLACEHOLDER`)
13. **Footer** — Praha · Brno · Bratislava · Wien

---

## BLOCKIERER — WARTEN AUF DICH (in Priorität)

### 🔴 High Priority — bevor irgendwas live geht

**1 · A/B-Entscheidung Voice.**
Original (poetisch) oder Hormozi-30% (direkt)? Beide simultan public bekommen geht nur über zwei URL-Pfade (Pages). Sonst muss eine gewinnen.
*Entscheidungs-Hilfe:* Original gewinnt bei intellektueller, älterer Audience (35-39). Hormozi gewinnt bei jüngerer, konversions-fokussierter Audience (25-32). Die Mitte könnte ein 50/50-Hybrid sein — sag wenn ich das bauen soll.

**2 · Tally-Form aufsetzen.** (~15 Min für dich)
- Felder die du brauchst: Vorname · Nachname · E-Mail · Alter (25-29 / 30-34 / 35-39 / andere) · Nationalität (SK / CZ / andere) · Geschlecht (M / F / andere) · Wie lang in Wien (<1J / 1-3 / 3-7 / 7+) · Beruf · Was suchst du? (langfristige Beziehung / offen / networking) · **Warum tento večer?** (offene Frage, max 200 Zeichen — qualifizierender Killer)
- Stripe-Integration: €29 Payment am Ende der Form (Tally hat das nativ)
- URL zurück an mich → ich plugge sie in beide index-Dateien (eine Stelle pro Datei)

**3 · Founder-Foto droppen.**
Datei: `cz-sk-vienna/founder.jpg`
Format: Porträt, ca. 280×360px Display-Größe (kann hochauflösender sein, wird responsive geskaliert)
Vibe: seriös aber warm, kein LinkedIn-Stocky. Du als Mensch, nicht als Operator.

### 🟡 Mid Priority — innerhalb 14 Tage

**4 · Lokation Wien 1. Bezirk fixieren.**
30 Personen, Mo-Abend 22.06.2026, 19-22 Uhr. Wenn fix → Site-Update auf konkrete Adresse. Bis dahin steht "Wien, 1. okres" als Platzhalter.

**5 · Domain entscheiden.**
Aktueller Platzhalter: `info@cs-dating.wien` im Footer. Tatsächliche Domain-Optionen: `cs-dating.wien` · `csdating.wien` · `cesko-slovensky.wien` · `kruh.wien` (falls Brand zurückgeflippt). Wenn fix, ich tausche im Footer + Title.

**6 · GitHub Pages aktivieren** (für permanente URL → Flyer-QR-Code).
Du machst das im Browser: jakub-ai23/ops → Settings → Pages → Branch `claude/review-vienna-report-Uvi1g`, /cz-sk-vienna als Source. Resultat: `jakub-ai23.github.io/ops/cz-sk-vienna/`. Ich kanns nicht via CLI/MCP — Repo-Setting.

**7 · Flyer bauen — du musst entscheiden:**
- A5 Print für Distribution in Slovak/Czech-Bars/Lokalen
- IG-Story 1080×1920 für digitale Verteilung
- Beides
*Default wenn du nicht antwortest:* beide. Entwurf von mir, du gibst Feedback.

### 🟢 Low Priority — strategisch

**8 · Voice-Profil-Kalibrierung Hormozi.**
Wenn du genauer willst: paste Hormozi-Profil-Auszug aus `~/Projects/content/voice-library/hormozi.md` → ich kalibriere Hormozi-Version präziser. Aktuell arbeite ich aus meinem Modellwissen (Sub-Repo `jakub-ai23/content` ist außerhalb meines MCP-Scopes).

**9 · CZ + EN-Übersetzungen.**
Erst wenn SK final-locked. Strukturell vorbereitet (V0-Scaffold im History committed), aber inhaltlich neu-schreiben weil Original nun völlig andere Tonalität hat.

---

## DISTRIBUTION-KANÄLE (aus Pidgeot-Recherche, ready für Flyer)

Verifiziertes Gold:
- **Slovak Institute Wien** (Wipplingerstraße 24-26) — physische Distribution
- **Czech Centre Wien / Tschechisches Zentrum** (Gußhausstraße 10) — physisch
- **FB Group** "Slováci a Češi vo Viedni" — digitale Reichweite
- **FB Group** "Slováci v Rakúsku" — digital
- **Slovaci.at** — Community-Portal, optional Werbung
- **Slovak PRO** — professionelles Networking, online-event-Push

Pidgeot bestätigt **Whitespace** ist real: kein dedizierter SK/CZ-Speed-Dating-Anbieter in Wien. USP hält.

---

## STRATEGISCHE FLAGS (Zoya watchlist)

| Guardrail | Status |
|-----------|--------|
| **G1 Mission Cap** | REAL TEAM geparkt → Mission-Slot frei. Kruh = Mission #3 mit Martina operativ. **D-Eintrag für REAL-TEAM-Parking steht aus** — sag mir die Reaktivierungs-Bedingung, ich logge die Decision-Zeile. |
| **G3 72h Novelty Lock** | ✅ Abgelaufen. Idee entstand 04.05, heute 07.05. Frei für Außenwirkung ab sofort. |
| **G6 Information Hygiene** | ✅ Hold. "30.000 Slowaken" *nicht* als Fakt in Copy. Frauen-Überhang von Martina (4-Tage-Connection) wurde nicht plakativ behauptet, sondern *strukturell* in der Pre-Ženu-Spalte verarbeitet (performance-flirteri = Lifestyle-beobachtbares Phänomen, nicht statistische Behauptung). |
| **G4 North Star Filter** | ✅ Pass. Revenue-Path (€29 × 30 = €870/event × 4 = €3,5K/yr — Hobby-Income, kein Mission-1-Ersatz). Health: neutral. Partnership-Conditions: **direkt positiv** (du bist im Raum). |
| **Daily Logs fehlen** | 05.05, 06.05, 07.05 unbeschrieben. Sag wenn ich 07.05 backfille mit deinen Health-Check-Inputs. |

---

## NÄCHSTE SCHRITTE (in Reihenfolge, für dich am PC)

1. **Beide Previews öffnen** — Original + Hormozi nebeneinander
2. **Voice-Entscheidung treffen** (oder mir sagen "bau Hybrid")
3. **Tally-Form bauen + URL schicken**
4. **Founder-Foto droppen** in `cz-sk-vienna/founder.jpg`
5. **Domain wählen**
6. **Lokation fixieren** (wenn schon klar)
7. **Pages aktivieren** wenn permanente URL gebraucht
8. **Flyer-Format entscheiden** (A5 / IG / beides)

## NÄCHSTE CLAUDE-SESSION

Bei Sessionstart erwarten dich:
- Tally-URL plug-in (1 Min wenn URL da)
- Founder-Foto check (automatisch sichtbar wenn Datei da)
- Brand-Swap-Discipline check (briefing.md → "Kruh" → "ČS Dating" finalisieren)
- Voice-Profile-Calibration falls gepasted
- Flyer bauen
- CZ + EN Übersetzungen wenn SK final
- Daily-Log 07.05 backfill mit deinen Inputs

---

## QUICK-LINKS

**Vorschau Mobile (htmlpreview):**
- Original: https://htmlpreview.github.io/?https://github.com/jakub-ai23/ops/blob/claude/review-vienna-report-Uvi1g/cz-sk-vienna/index.html
- Hormozi: https://htmlpreview.github.io/?https://github.com/jakub-ai23/ops/blob/claude/review-vienna-report-Uvi1g/cz-sk-vienna/index-hormozi.html
- Logo: https://htmlpreview.github.io/?https://github.com/jakub-ai23/ops/blob/claude/review-vienna-report-Uvi1g/cz-sk-vienna/logo.html

**GitHub Branch:**
https://github.com/jakub-ai23/ops/tree/claude/review-vienna-report-Uvi1g/cz-sk-vienna

**Branch-Name (für Pull/Checkout):**
`claude/review-vienna-report-Uvi1g`

---

*Konversations-Thread war lang. Nicht von vorn anfangen — der nächsten Claude-Session reicht: "Read SITREP.md in cz-sk-vienna/" und sie ist im Bilde.*
