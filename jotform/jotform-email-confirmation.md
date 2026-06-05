# Jotform Auto-Confirmation Email — ČS Dating Edícia I

Sent automatically after every successful form submission.
Configure in Jotform: Settings → Emails → Notifier (to applicant) → Edit.

---

## Subject line options (pick one)

**A. Direct:**
```
Dostali sme tvoju prihlášku — ČS Dating Wien
```

**B. Warmer:**
```
Tvoja prihláška dorazila. Ozveme sa do 24 hodín.
```

**C. Branded:**
```
ČS Dating · Edícia I — prihláška prijatá
```

**My pick: B.** Sets expectation in the subject = open rate insurance + lower anxiety.

---

## Body (Slovak — paste into Jotform email body, HTML mode)

```html
<div style="font-family:Inter,-apple-system,sans-serif;max-width:540px;margin:0 auto;color:#0d0d0d;line-height:1.65;">

  <h2 style="font-family:'Cormorant Garamond',Georgia,serif;font-size:1.7rem;font-weight:600;color:#0d0d0d;border-left:3px solid #8b2252;padding-left:14px;margin:0 0 18px;">Dostali sme tvoju prihlášku.</h2>

  <p style="font-size:0.96rem;margin:0 0 14px;">Ahoj {firstName},</p>

  <p style="font-size:0.96rem;margin:0 0 14px;">Ďakujeme za prihlášku na <strong>ČS Dating Wien — Edíciu I</strong> (22. júna 2026).</p>

  <p style="font-size:0.96rem;margin:0 0 14px;">Tvoje údaje sme prijali a momentálne ich prechádzame. Overujeme každú prihlášku osobne, kvôli balansu (10 mužov + 10 žien) a kvôli bezpečnosti všetkých účastníkov.</p>

  <p style="font-size:0.96rem;margin:0 0 14px;"><strong>Do 24 hodín ti napíšeme</strong>:</p>

  <ul style="font-size:0.94rem;margin:0 0 18px;padding-left:20px;">
    <li>či si prijatý/á</li>
    <li>presnú adresu venue (Wien, 1. okres)</li>
    <li>časový harmonogram večera</li>
    <li>info o platbe (ak ešte nebola)</li>
  </ul>

  <p style="font-size:0.96rem;margin:0 0 14px;">Ak máš medzitým otázku, odpíš priamo na tento email.</p>

  <p style="font-size:0.96rem;margin:0 0 22px;">Tešíme sa.<br>
  <strong>Jakub & Martina</strong><br>
  <em style="color:#6b5540;font-size:0.86rem;">ČS Dating Wien</em></p>

  <hr style="border:none;border-top:1px solid rgba(139,34,82,0.18);margin:24px 0;">

  <p style="font-size:0.78rem;color:#6b5540;line-height:1.55;margin:0;">
    <strong>Prečo overenie?</strong> Prísny výber účastníkov je dôvod, prečo to funguje. Vyberáme podľa veku (25–39), pôvodu (SK/CZ), zámeru a profesionálneho profilu (LinkedIn). Ak nezapadáš, €39 ti vrátime do 72 hodín. Bez otázok.
  </p>

  <p style="font-size:0.74rem;color:#6b5540;margin:18px 0 0;letter-spacing:0.5px;">
    🔒 Platba bezpečne cez Stripe &nbsp;·&nbsp; 💸 €39 späť ak nezapadáš &nbsp;·&nbsp; 📍 Wien, 1. okres
  </p>

</div>
```

---

## Plain-text fallback (in case email client strips HTML)

```
Ahoj {firstName},

Dostali sme tvoju prihlášku na ČS Dating Wien — Edíciu I (22. júna 2026).

Tvoje údaje sme prijali a momentálne ich prechádzame. Overujeme každú prihlášku osobne, kvôli balansu (10 mužov + 10 žien) a kvôli bezpečnosti všetkých účastníkov.

Do 24 hodín ti napíšeme:
- či si prijatý/á
- presnú adresu venue (Wien, 1. okres)
- časový harmonogram večera
- info o platbe

Ak máš medzitým otázku, odpíš priamo na tento email.

Tešíme sa.
Jakub & Martina
ČS Dating Wien

—

Prečo overenie? Prísny výber účastníkov je dôvod, prečo to funguje. Vyberáme podľa veku (25–39), pôvodu (SK/CZ), zámeru a profesionálneho profilu (LinkedIn). Ak nezapadáš, €39 ti vrátime do 72 hodín. Bez otázok.
```

---

## Jotform setup notes

1. **Settings → Emails → Notifier**
2. **Recipient email:** `{Email}` (the form's email field — Jotform variable)
3. **Reply-To:** `info@cs-dating.wien` (or your Gmail until domain is set up)
4. **Subject:** paste option B above
5. **Body:** switch to HTML view → paste the `<div>` block
6. **Test:** submit yourself, check it lands and renders. Open on mobile too.

## What's intentionally NOT in this email

- ❌ Venue address — you don't have it yet. Stays in the next-step email.
- ❌ Exact start time — only "harmonogram večera" mentioned. Confirm 19:30–21:30 when sending the second email.
- ❌ Payment confirmation — Jotform sends a separate Stripe receipt automatically. Don't duplicate.
- ❌ Calendar .ics file — premature. Add to email #2 after acceptance.

---

## Next email to draft (when you're ready)

**Email #2 — Acceptance + venue + agenda.** Sent manually by you within 24h after review. I'll draft this when venue is locked. Triggers needed:
- Venue address confirmed
- 24h review process (you/Martina go through LinkedIn, employment, fit)
- Standardized template so you can fire it in 30 sec per accepted applicant
