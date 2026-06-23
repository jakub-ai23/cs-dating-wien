# Translation Mission Report — ČS Dating Wien · SK → DE

**Created:** 2026-06-23
**Pipeline:** translate-document skill (glossary-driven, multi-agent QA)
**Source:** SK-Root (`docs/index.html` + 3 Legal-Seiten), Cross-Ref EN
**Target:** Österreichisches Deutsch (AT) · Anrede Du (großgeschrieben)
**Decisions (Commander, 2026-06-23):** AT-Dialekt · Quelle SK · Du groß · Edícia→Edition · DSGVO §7 slowakische Behörde originalgetreu · volle Integration

---

## Erzeugte Dateien (alle unter `docs/`, GitHub-Pages-Quelle)

| Datei | Inhalt |
|---|---|
| `de/index.html` | Landing (volle Verkaufsseite, 9-Movement-Reise) |
| `de/impressum/index.html` | Impressum |
| `de/terms/index.html` | Teilnahmebedingungen |
| `de/privacy-policy/index.html` | Datenschutz |

## Integration (bestehende Seiten angepasst)
- `index.html` (SK), `cs/index.html` (CZ), `en/index.html` (EN): je `hreflang="de"` + `og:locale:alternate de_AT` + 🇩🇪 im Sprachumschalter.
- `sitemap.xml`: de-hreflang in alle Blöcke + neuer `/de/`-Eintrag.
- `llms.txt`: deutsche Seite in Sprachliste ergänzt.
- DE-Landing selbst: `lang=de`, canonical/og/JSON-LD auf `/de/`, Toggle DE aktiv, Footer-Links auf `/de/`-Legal.

## Assets (wiederverwendbar)
- `translation/glossary_sk_de.md` — Begriffskarte (Marke, Term-Map, Locked-Hooks, Format, Layout-Risiko).
- `translation/2026-06-23-proofreader-iter1.md` — AT-Korrektorat.
- `translation/preview-de-full.png`, `preview-de-impressum.png` — Previews.

---

## QA-Ergebnis

**Translator (2 Agenten):** Landing + Legal getrennt, in-place, glossargesteuert.
**Proofreader (AT-Muttersprachler):** **SHIP-READY** — 0 CRITICAL, 0 HIGH, 2 MED, 4 LOW. Einziger Fix: 3× gerades schließendes Anführungszeichen → deutsches „…" (erledigt).
**Gatekeeper (mechanisch):**
- Strukturparität Landing SK vs DE: alle Element-Counts identisch (sections/div/p/h2/a/img/script/faq-item). ✓
- Legal-Parität (h2/p/li/tr): identisch. ✓
- JS intakt (Seat-Counter, Countdown, Typewriter, Waitlist-Popup). ✓
- IDs/Links/Mails/Beacon/EDITION1 unverändert. ✓
- Währung durchgehend „NN €" (0× „€NN"). ✓
- Datum AT (22. Juni 2026 / Montag / 17. Mai 2026). ✓
- Keine SK-Reste im gerenderten Text (einziger Treffer: auskommentierter Dev-Block, nicht gerendert). ✓
- Keine Gedankenstriche im Fließtext (nur erlaubte Zahl-/Zeitbereiche; Countdown-Separatoren auf „·" umgestellt). ✓

**Preview:** Hero rendert sauber (Hook, Meta-Strip, CTAs, Authority-Zeile) — keine Layout-Overflows an den Glossar-§7-Risikostellen. Impressum rendert sauber. Event-Card visuell nicht headless-screenshotbar (100vh-Hero + Anchor-Scroll), Textlängen aber unkritisch und CSS identisch zur Live-SK-Card.

---

## Offene Punkte für den Commander
1. **Seat-Zahlen-Diskrepanz (KEIN Übersetzungsfehler):** Labels/JS sagen „Männer 6 / Frauen 7" (= SK-Quelle), CLAUDE.md notiert „7 men / 6 women". Existiert 1:1 in der SK-Quelle → Datenpflege, nicht Übersetzung.
2. **DSGVO §7:** auf Wunsch slowakische Behörde belassen. Falls später österreichische DSB gewünscht → ein Wort.
3. **Deploy:** Push = live. Noch NICHT gepusht. Lokaler Preview lief auf `:8791` (gestoppt).

**VERDIKT: SHIP-READY.** Wartet auf Deploy-Freigabe.
