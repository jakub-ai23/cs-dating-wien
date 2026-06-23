# Korrektorat — ČS Dating Wien · DE-Seiten (Iteration 1)

**Erstellt:** 2026-06-23
**Korrektor:** Muttersprachlicher AT-Korrektor (Wien)
**Geprüft:** `docs/de/index.html` · `docs/de/impressum/index.html` · `docs/de/terms/index.html` · `docs/de/privacy-policy/index.html`
**Gegen:** SK-Quellen `docs/index.html` + 3 Legal-Seiten · Glossar `translation/glossary_sk_de.md`
**Methode:** Seite-für-Seite Abgleich SK→DE, Glossar-Treue, Dash-Sweep (grep), Quote-Sweep (grep), Währungs-/Datums-Sweep (grep).

---

## Zusammenfassung

| Schweregrad | Anzahl |
|---|---|
| CRITICAL | 0 |
| HIGH | 0 |
| MED | 2 |
| LOW | 4 |

**Gesamturteil: SHIP-READY.**

Die Übersetzung ist auf Publikationsniveau. Sie liest sich durchgehend wie von einem Wiener Muttersprachler geschrieben, nicht wie eine Übersetzung. Hormozi-Punch in den Hooks ist erhalten. Alle Verbindlichkeiten (Preis, Storno, Garantie, DSGVO-Fristen) sind 1:1 zur SK-Quelle. Du-Form durchgehend großgeschrieben. Keine Gedankenstrich-Verstöße im gerenderten Text. Keine slowakischen Resttexte. Glossar verbatim eingehalten (Edícia→Edition, Marke bleibt, Welcome Drink, geheimer Ort, Mystery Location, halušky bleibt).

Die MED/LOW-Funde sind reine Politur, kein Blocker. **Empfehlung: ausliefern; die zwei MED-Punkte bei Gelegenheit nachziehen.**

---

## Datei 1 — `docs/de/index.html` (Landing)

**Urteil: SHIP-READY.** Glossar-Treue exzellent, Verkaufsrhythmus erhalten.

### MED

**[MED] Deutsche Anführungszeichen: schließendes Zeichen falsch (4× gesamt, hier 1×)**
- Zeile 1811 (Ist): `seltsamer Humor, denkst Du Dir, „das liegt wohl an der Sprache. Ich gebe ihm eine Chance, er wirkt ganz fähig.“`
  - Hier ist das ÖFFNENDE Zeichen am Satzende verwendet (`.“`) statt des schließenden `."`. Korrektes Paar: `„… fähig.“` ist falsch herum — DE öffnet mit `„` (unten) und schließt mit `"` (oben). Ist-Zustand öffnet mit `„` (Z1811 Anfang, korrekt) und schließt mit `“` — das ist eigentlich das KORREKTE deutsche schließende Zeichen. **Hinweis:** dieses Vorkommen ist tatsächlich korrekt deutsch („…fähig.") Kein Fund. (Siehe stattdessen Z1896 unten.)
- Zeile 1896 (Ist): `…dass Familie nicht „zu viel" ist.`
  - Schließendes Zeichen ist gerades `"` statt deutsches `"`. **Vorschlag:** `nicht „zu viel" ist.` Konsistenz mit Z1811. (Gehört zur seitenübergreifenden Quote-Inkonsistenz, siehe Sammelfund unten.)

### LOW

**[LOW] „60 % der Menschen wurden geghostet"** (Z1794) — SK: „60 % ľudí bolo ghostnutých." Inhaltlich + Glossar korrekt (geghostet laut Term-Map). Stilistisch in einer Ich-Erzählung etwas statistisch-trocken, aber identisch zur SK-Absicht. Kein Eingriff nötig.

**[LOW] „Sieh Dir das Format an →"** (Z1702) vs SK „Pozri si formát →" — Natürlich, gut. Kein Fund, nur Bestätigung.

**Positiv bestätigt (keine Funde):**
- H1 / Title / OG: „Online hast Du einen Versuch. Live hast Du einen ganzen Abend." — exakt nach Locked-Rhythm-Phrase.
- Alle Locked-Rhythm-Phrasen vorhanden und korrekt: „Du weißt, wie es ausgegangen ist." · „Es ist keine Frage des Ob…/Hier." · „Zwei Länder./Eine gemeinsame Welt." · „Apps urteilen über Dich…/Wir geben Dir einen Abend." · „Kein weiteres Speed-Dating." · „20 Menschen. Ein Abend. Niemand muss Weihnachten erklären." · „Maximal 10 Dates an einem Abend. Das Gefühl macht den Rest." · „Menschen, kein Algorithmus." · „Wir wählen aus. Wir prüfen. Wir schützen Dich." · „Sichere Dir Deinen Platz." · „Wenn voll, dann voll." · cta-soft „volle Rückerstattung, keine Fragen."
- Countdown-JS-Strings (Z2323-2327, 2401-2405): „noch X Tage Y h / noch 1 Tag / letzte X Min / endet jetzt" — exakt nach Glossar §4, KEIN Gedankenstrich (SK hatte „— ešte"; DE korrekt auf „ · noch" umgestellt). Sehr saubere Lokalisierung.
- Währung durchgehend „69 €/39 €/−30 €" (Symbol nach Betrag) — Glossar §5 erfüllt. (SK-Quelle hatte „€69" — in DE korrekt gedreht.)
- Datum: „22. Juni 2026", „Montag", „22.6.2026", „22. Juni" (Countdown) — konsistent, AT-Locale.
- Du-Form durchgehend groß (Du/Dir/Dein/Dich), auch FAQ-Plural „wie Ihr Euch am Tisch einigt" korrekt als Gruppe.
- Footer-Separator auf „·" gesetzt (SK Z2229 hatte „–" als Trenner: „Wien – Speed dating"); DE Z2231 nutzt „·". Gut, Gedankenstrich vermieden.
- Gedankenstrich-Sweep: alle — / – nur in HTML-/JS-Kommentaren, schema.org `alternateName` (Markenstring, egal), Eyebrow-Deko `— "` (Z1954, dekoratives Zeichen, kein Fließtext) und erlaubten Zahl-/Zeitbereichen (25–39, 19:30 – 21:30). **Keine Verstöße.**

**[LOW] Inhaltlicher Hinweis (KEIN Übersetzungsfehler, in SK identisch):** Seat-Row-Labels vs JS-Konstanten sind vertauscht. Z2013 Label „Männer · 6 von 10", Z2017 „Frauen · 7 von 10"; JS Z2247 `MEN_TAKEN=6, WOMEN_TAKEN=7`. Konsistent, ABER: das Hero-Meta (Z1687) sagt „Frauen · Männer" und CLAUDE.md führt „7 men / 6 women". Diese Diskrepanz existiert 1:1 in der SK-Quelle und ist KEINE Übersetzungssache, nur zur Kenntnis für den Commander (Datenpflege, nicht Korrektorat).

---

## Datei 2 — `docs/de/impressum/index.html`

**Urteil: SHIP-READY.** Keine Funde.

- Term-Map korrekt: Organizátor→Veranstalter, Účastnícky príspevok→Teilnahmebeitrag, Storno podmienky→Stornobedingungen, Rakúsko→Österreich.
- Preis-Verbindlichkeit 1:1: „69 € … Code EDITION1 … um 30 € … Welcome Drink … Endbetrag 39 €" = SK „69 € … o 30 € … 39 €".
- 48-Stunden-Frist (Adresse) erhalten (Z65).
- Datum „17. Mai 2026" (AT) korrekt aus „17. máj 2026".
- Du-Form groß. Keine Gedankenstriche. Keine Anführungszeichen auf der Seite.
- Adresse/Telefon/E-Mail/IDs unverändert (Glossar §2).

---

## Datei 3 — `docs/de/terms/index.html` (Teilnahmebedingungen)

**Urteil: SHIP-READY.** Alle Rechts-Verbindlichkeiten 1:1.

### LOW

**[LOW] Deutsche Anführungszeichen: schließendes Zeichen gerade statt deutsch**
- Zeile 82 (Ist): `…die unverbindlich „nur mal vorbeischauen" möchten.`
  - **Vorschlag:** `„nur mal vorbeischauen"` (deutsches schließendes Zeichen `"`). SK-Quelle hatte dieselbe SK-Konvention (`„…"`), wurde mit-übernommen. Teil des Sammelfunds unten.

**Positiv bestätigt (Verbindlichkeiten alle korrekt):**
- §4: „in voller Höhe innerhalb von 72 Stunden … auf die ursprüngliche Zahlungsart" = SK „celá suma … do 72 hodín na pôvodný spôsob platby". 
- §5 Storno-Tabelle vollständig + bedeutungsgleich: 100 % / 72 h · 7+ Tage → Gutschein voller Wert · <7 Tage → kein Anspruch · Krankheit+Attest 24 h → Gutschein. „voucher"→„Gutschein" (Glossar). „edíciu"→„Edition".
- §5-Begründung 7-Tage-Grenze inhaltlich identisch.
- §9 Höhere Gewalt: „Gutschein … oder … volle Rückerstattung" = SK „voucher … plné vrátenie peňazí".
- §10 Rozhodné právo: „Recht der Republik Österreich … Gericht in Wien" = SK 1:1. (Österreich-Recht bleibt, korrekt.)
- Datum „17. Mai 2026". Du-Form groß. Keine Gedankenstriche.

---

## Datei 4 — `docs/de/privacy-policy/index.html` (Datenschutz)

**Urteil: SHIP-READY.** DSGVO-Zitierweise korrekt, Fristen 1:1.

### LOW

**[LOW] Deutsche Anführungszeichen: schließendes Zeichen gerade statt deutsch**
- Zeile 105 (Ist): `Die Löschung zu verlangen („Recht auf Vergessenwerden", Art. 17)`
  - **Vorschlag:** `(„Recht auf Vergessenwerden", Art. 17)`. Teil des Sammelfunds unten.

**Positiv bestätigt:**
- DSGVO-Zitierweise korrekt umgestellt (Glossar §5): SK „čl. 6 ods. 1 písm. b)" → DE „Art. 6 Abs. 1 lit. b" (lit. b/f, Art. 9/15/16/17/18/20/21 alle korrekt). „Nariadenie (EÚ) 2016/679 (GDPR)" → „Verordnung (EU) 2016/679 (DSGVO)". „GDPR"→„DSGVO" durchgehend.
- §5 Aufbewahrungsfristen 1:1: 14 Tage (abgelehnt) · 30 Tage (bestätigt) · 6 Monate (E-Mail) · Stripe nach gesetzlicher Pflicht (AML).
- §6 Antwortfrist „innerhalb von 30 Tagen" = SK „do 30 dní".
- §7: verweist BEWUSST auf „Amt für den Schutz personenbezogener Daten der Slowakischen Republik" = SK 1:1. **Laut Brief + Glossar §8 Commander-Entscheidung LOCKED — KEIN Fehler, nicht beanstandet.**
- §4 Auftragsverarbeiter (Jotform/Stripe/GitHub/Google), Länder, SCC + EU-US DPF: alle korrekt.
- §2: „Art. 9 DSGVO" (besondere Kategorien) korrekt aus „čl. 9 GDPR".
- Datum „17. Mai 2026". Du-Form groß. Keine Gedankenstriche.

---

## Sammelfund (seitenübergreifend)

**[MED] Deutsche Anführungszeichen — schließendes Zeichen uneinheitlich**

Im gerenderten Text gibt es 4× das öffnende deutsche „ (unten). Davon schließt nur 1× korrekt mit dem deutschen " (oben), 3× mit geradem `"`:

| Datei | Zeile | Ist | Soll |
|---|---|---|---|
| index.html | 1811 | `„das liegt … fähig.“` | korrekt (deutsches Paar „…") — KEIN Fund |
| index.html | 1896 | `„zu viel"` | `„zu viel"` |
| terms/index.html | 82 | `„nur mal vorbeischauen"` | `„nur mal vorbeischauen"` |
| privacy-policy/index.html | 105 | `„Recht auf Vergessenwerden"` | `„Recht auf Vergessenwerden"` |

**Ursache:** Aus der SK-Quelle übernommen (SK nutzt `„…"` mit geradem Schluss). Für publikationsreifes Deutsch sollte durchgängig das Paar `„ … "` stehen. **Eingestuft als MED, nicht HIGH:** rein typografisch, ändert keine Bedeutung, fällt nur dem geschulten Auge auf. Fix = 3 Zeichen-Ersetzungen.

---

## Geprüft und unkritisch

- **Vollständigkeit:** Kein slowakischer Resttext im gerenderten Bereich. `lang="de"` korrekt auf allen 4 Seiten. Sprachumschalter mit DE-Eintrag aktiv (index Z1653).
- **Eigennamen/Marke:** Česko-Slovenský Dating, ČS Dating, Wien, EDITION1, Welcome Drink, Open End, Jakub Popluhar, Martina Nováková, Jotform/Stripe/GitHub/Google — alle unverändert. ČS bleibt ČS (nicht „Tschechisch-Slowakisch").
- **AT-Marker:** ß korrekt (ausschließlich, größtmöglicher, lässt, müssen — kein CH-ss). Keine störenden reichsdeutschen Marker. „Jänner" nicht relevant (kein Januar im Text).
- **Hreflang:** index Z16 ergänzt `hreflang="de"` korrekt; x-default bleibt EN.
