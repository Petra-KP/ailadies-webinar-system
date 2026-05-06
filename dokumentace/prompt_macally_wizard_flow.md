# Prompt pro Macally – změna objednávkového flow AILadies

---

## Zadání

Zachovej veškerý vizuál stránky přesně tak, jak ho máš aktuálně postavený – barvy, fonty, layout, styly karet, tlačítek, formulářových polí, vše. Nic vizuálního nemaž ani nepřepisuj.

Změn pouze **logiku a pořadí kroků v objednávkovém flow** – konkrétně sekce `#nabidka` a `#zacit`.

---

## Co se má změnit

### 1. Sekce `#zacit` – přestavět na multi-step wizard

Nahraď stávající jeden dlouhý formulář třemi kroky. Stepper (číslované kroky nahoře: 1 / 2 / 3) přidej ve stylu, který odpovídá zbytku stránky.

---

**Krok 1 – Vyber, jak chceš začít**

Zobraz tři klikatelné karty (použij stávající styl karet/balíčků):

- **Zdarma** – Úvodní konzultace (20 min) – bez ceny
- **Jednorázové setkání** – 3 000 Kč / 60 min
- **Balíček** – zobraz sub-výběr: Start (8 550 Kč) / Rozjezd (13 800 Kč) / Proměna (26 100 Kč)

Po kliknutí na kartu se zvýrazní (stejný efekt jako `.featured` u balíčků).

Tlačítko „Pokračovat →" se aktivuje až po výběru.

Speciální chování:
- Pokud klientka vybere **Zdarma** → Krok 2 se přeskočí, rovnou se zobrazí Krok 3-A (bez formuláře, bez platby)
- Pokud vybere **Jednorázové nebo Balíček** → zobrazí se Krok 2

---

**Krok 2 – Řekni mi o sobě** (zobrazí se jen u placených produktů)

Přesuň sem veškerý obsah stávajícího formuláře – žádné pole nemaž. Rozděl ho do dvou vizuálních bloků:

**Blok A – základní info (povinné):**
- Jméno a příjmení
- E-mail
- Pracovní role nebo pozice
- Obor nebo firma

**Blok B – diagnostika (volitelné, doporučené):**
- Jak vypadá tvůj typický pracovní den?
- Co tě v práci nejvíc unavuje nebo zabírá čas?
- Co tě baví a kde se cítíš sebejistě?
- Jak na tom jsi s AI? (radio)
- Jak ses s AI dostala do kontaktu? (radio)
- Jaké AI nástroje používáš? (checkboxy)
- Co od mentoringu očekáváš? (textarea)
- Kolik hodin mentoringu tě zajímá? (zachovat stávající widget s čísly 1–10 + balíčky)
- Nahrání hlasové zprávy (volitelné)
- Jak ses o AILadies dozvěděla? (checkboxy)
- GDPR checkbox (povinný)

Tlačítko „Odeslat a pokračovat →" odešle data formuláře a zobrazí Krok 3.

---

**Krok 3 – Potvrzení + rezervace**

Obsah se liší podle výběru z Kroku 1:

**Varianta A – Zdarma:**
- Text: „Skvěle! Rezervuj si termín úvodní konzultace přímo v kalendáři."
- Tlačítko: `👉 Rezervovat konzultaci zdarma` → odkaz: `https://calendar.app.google/AL6XEoUVpUE3uc9p6`
- Žádné platební info, žádný QR kód

**Varianta B – Jednorázové setkání nebo Balíček:**
- Text: „Tvoje žádost je odeslaná. Zaplať a rezervuj si termín – pak se potkáme."
- Zobraz název a cenu vybraného produktu (např. „Rozjezd · 5 setkání · 13 800 Kč")
- Platební box: zobraz statický QR kód z obrázku + číslo účtu
  - QR soubory jsou v: `assets/qr_3000.png`, `assets/qr_8550.png`, `assets/qr_13800.png`, `assets/qr_26100.png`
  - JavaScript vybere správný soubor podle zvolené ceny
- Text pod QR: „Termín si rezervuj hned – fakturu dostaneš e-mailem. Uhraď ji prosím před prvním setkáním."
- Tlačítko: `📅 Vybrat termín mentoringu v kalendáři` → odkaz: `https://calendar.app.google/rRpr1pQGoHsRc8jJ9`

---

### 2. Sekce `#nabidka` – tři změny

**a) Přepiš text tří procesních kroků (01 / 02 / 03) v úvodu sekce:**

- 01: **Vyber, jak začít** – „Klikni na produkt, který tě zajímá – nebo začni zdarma 20minutovou konzultací."
- 02: **Řekni mi o sobě** – „Vyplň krátký formulář. Pomůže mi připravit se – a hned od začátku pracujeme na tvém tématu."
- 03: **Vyber termín v kalendáři** – „Vyber termín v kalendáři a potvrď rezervaci. Fakturu dostaneš e-mailem – uhraď ji prosím před prvním setkáním."

**b) CTA tlačítka u každého produktu – sjednotit:**

- **Zdarma** – tlačítko zůstane beze změny (přímý odkaz na kalendář)
- **Jednorázové setkání** – tlačítko „Chci jednorázový mentoring" → při kliknutí scrollne na `#zacit` A přednastav Krok 1 na „Jednorázové setkání"
- **Balíčky** – každý balíček (Start / Rozjezd / Proměna) dostane tlačítko „Chci [název balíčku]" → scrollne na `#zacit` A přednastav Krok 1 na daný balíček

**c) Odeber `offer-cta-row`** – blok se třemi tlačítky úplně dole v sekci `#nabidka` (Vyplnit formulář / Úvodní konzultace – kalendář / Mentoring – kalendář). Tato volba je nově součástí wizardu.

---

## Co se nesmí změnit

- Veškerý vizuál: barvy, fonty, odsazení, styly tlačítek, karet, formulářů
- Sekce: hero, pro-koho, jak-to-funguje, co-dostanes, o-mne, moje-praxe, share, footer
- Obsah a texty produktů (ceny, benefity, popisy balíčků)
- Žádné pole formuláře se nemaže – jen se přesouvají do Kroku 2

---

## Technické poznámky

- Krok 1 / 2 / 3 jsou přepínané JavaScriptem (hide/show), vše na jedné stránce
- Výběr z Kroku 1 se uchovává v JS proměnné a čte se v Kroku 3 (pro zobrazení správného QR + kalendářního odkazu)
- Přednastav Krok 1 z externího odkazu pomocí URL parametru nebo funkce, kterou zavoláš z CTA tlačítka v `#nabidka`
