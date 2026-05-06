# Zadání pro Macaly: úpravy hero sekce – AILadies

**Stránka:** [ailadies.cz](https://www.ailadies.cz/)
**Priorita:** vysoká
**Rozsah změn:** hero (hlavní sekce), tlačítka, pohyblivá lišta, cena/ocenění

---

## Přehled změn (co a kde)

| # | Co se mění | Kde na stránce |
|---|---|---|
| 1 | Pravý blok (dark karta „Proč AILadies?") → **fotka** | Hero, pravá strana |
| 2 | Jméno Petry **pod fotografií** | Pod fotkou |
| 3 | Tlačítko „Chci začít" → nový text | Hero, primární CTA |
| 4 | Tlačítko „Jak to funguje" → nový text | Hero, sekundární CTA |
| 5 | **Ikonky 1:1 / online / tvým tempem** přesunout pod tlačítka | Hero, levá strana – pod CTA tlačítky |
| 6 | Nová **pohyblivá lišta** (marquee/ticker) | Hned pod hero sekcí |
| 7 | **Ocenění / plaketa** Women Changing the World 2025 | Pod pohyblivou lištou NEBO na konci stránky do sekce „O mně" |

---

## Detailní popis každé změny

---

### Změna 1 – Pravý blok: nahradit dark kartu fotografií

**Aktuální stav:**
Pravá strana hero sekce obsahuje tmavou kartu s textem „Proč AILadies?" a třemi ikonkami (1:1, online, tvým tempem).

**Nový stav:**
Tmavou kartu **kompletně smazat** a místo ní vložit **fotografii Petry**.

**Specifikace fotografie:**
- Formát: výška 1,2–1,5× šířka (na výšku, portrétní).
- Zaoblené rohy: stejný radius jako ostatní karty na webu (Macaly volba „rounded" nebo „extra rounded").
- Pokud Macaly umožňuje shadow: přidat jemný stín (soft shadow).
- Fotografie by měla vyplnit celou pravou stranu layoutu – stejně velkou plochu, jakou zaujímala původní karta.

---

### Změna 2 – Jméno Petry pod fotografií

**Co přidat:**
Pod fotografii (nebo na spodní část fotografie jako overlay) vložit:

```
Petra Květová Pšeničná
Mentorka AI · Moderátorka · Spoluzakladatelka Fandi mámám
```

**Formátování:**
- Jméno: větší text, tučné nebo serif (stejný styl jako nadpisy na webu).
- Popisek pod jménem: menší text, světlejší barva (muted – zlatá/béžová, která se používá jinde na webu).
- Zarovnání: na střed nebo doleva (konzistentní s layoutem).

---

### Změna 3 – Ikonky „1:1 / online / tvým tempem" – přesunout, nesmazat

**Důležité:** Tyto ikonky jsou momentálně uvnitř dark karty (Proč AILadies?), která se maže. **Nesmazat obsah – přesunout ho** na levou stranu hero sekce, pod CTA tlačítka.

**Co přesunout (přesný text):**

| Hodnota | Popis |
|---|---|
| **1:1** | přizpůsobeno jen tobě |
| **online** | odkudkoliv |
| **tvým tempem** | žádný spěch |

**Jak to má vypadat:**
Tři ikonky/sloupce vedle sebe, horizontálně, každá s tučnou hodnotou nahoře a světlejším popiskem dole. Styl zachovat stejný jako jsou nyní v dark kartě – jen přesunout na levou stranu.

**Umístění:** přímo pod dvěma CTA tlačítky, jako součást levého sloupce hero.

---

### Změna 4 – Primární CTA tlačítko

**Aktuální text:** `Chci začít`

**Nový text:** `Konzultace zdarma (20 min)`

- Barva a styl tlačítka: beze změny (zlatá, plná).
- Odkaz: beze změny (stávající formulář nebo Google Calendar rezervace).

---

### Změna 5 – Sekundární CTA tlačítko

**Aktuální text:** `Jak to funguje`

**Nový text:** `Jak mentoring probíhá →`

- Barva a styl: beze změny (outline tlačítko).
- Odkaz: beze změny (kotva na sekci „Jak to funguje").

---

### Změna 6 – Pohyblivá lišta (marquee / ticker)

**Umístění:** Samostatná lišta **hned pod hero sekcí**, přes celou šířku stránky.

**Barva pozadí lišty:** tmavá (černá nebo tmavě zlatá, stejná jako accent barva webu – navrhuju `#1F1B16` nebo shodnou s dark kartou, která se maže).

**Barva textu:** zlatá nebo bílá (kontrastní k tmavému pozadí).

**Rychlost pohybu:** pomalá až střední – přehrává se donekonečna zprava doleva.

**Obsah lišty (přesný text, kopírovat přesně):**

```
✦ AI nadšenkyně  ✦ Mentorka AI  ✦ Moderátorka  ✦ Facilitátorka  ✦ Spoluzakladatelka Fandi mámám  ✦ Novinářka  ✦ Podcasterka – Dobro skladem  ✦ Mediální tréninky  ✦ AI nadšenkyně  ✦ Mentorka AI  ✦ Moderátorka  ✦ Facilitátorka  ✦ Spoluzakladatelka Fandi mámám  ✦ Novinářka  ✦ Podcasterka – Dobro skladem  ✦ Mediální tréninky
```

*(Text se opakuje, aby bylo plynulé přehrávání bez přerušení.)*

**Výška lišty:** cca 48–56 px.

**Padding textu:** 0 px od okraje (text jde přes celou šířku bez mezer po stranách).

> Pokud Macaly nemá nativní marquee/ticker komponentu, lze použít **Text Strip / Scrolling Banner** – hledej v elementech jako „Ticker", „Marquee", „Scrolling Text" nebo „Text Band".

---

### Změna 7 – Ocenění Women Changing the World 2025

**Co přidat:**
Logo plakety (zlatý medailon) s textem o ocenění.

**Soubor s logem je připraven:** `assets/winner_women_changing_world_2025.png` (uložen ve složce projektu).

**Varianta A – vedle jména pod fotkou (doporučeno):**
Zlatý medailon umístit napravo od jména Petry – malý, cca 64×64 px. Text vedle medailonu:

```
Women Changing the World
Winner 2025 · Czech & Slovak
```

**Varianta B – v sekci „O mně" (záložní):**
Přidat jako samostatný prvek do sekce O mně, vedle nebo pod popisem Petry. Velikost: cca 100×100 px.

**Formátování textu (pro obě varianty):**
- Malé písmo (cca 11–12 px).
- Zlatá barva textu (konzistentní s goldovými prvky webu).
- Zarovnání: na střed nebo vlevo vedle loga.

---

## Vizuální reference nového layoutu (schéma)

```
┌─────────────────────────────────────────────────────────────┐
│  NAV: AILadies          [Konzultace zdarma]                 │
├─────────────────────────────────────────────────────────────┤
│                        HERO                                 │
│                                                             │
│  ✦ OSOBNÍ AI MENTORING           ┌─────────────────────┐   │
│                                  │                     │   │
│  AI krok za krokem.              │    FOTKA PETRY      │   │
│  Tvým tempem.                    │    (portrétní)      │   │
│  S viditelnými výsledky.         │                     │   │
│                                  │  Petra Květová      │   │
│  Osobní mentoring pro ženy...    │  Pšeničná           │   │
│                                  │  Mentorka · Modr.   │   │
│  [Konzultace zdarma (20 min)]    │  🏅 Women Changing  │   │
│  [Jak mentoring probíhá →]       │     World 2025      │   │
│                                  └─────────────────────┘   │
│  1:1              online         tvým tempem                │
│  přizpůsobeno     odkudkoliv     žádný spěch                │
│  jen tobě                                                   │
├─────────────────────────────────────────────────────────────┤
│  ✦ AI nadšenkyně ✦ Mentorka AI ✦ Moderátorka ✦ ... →→→   │  ← LIŠTA
├─────────────────────────────────────────────────────────────┤
│  (zbytek stránky beze změny)                                │
└─────────────────────────────────────────────────────────────┘
```

---

## Checklist pro Macaly

- [ ] Dark karta „Proč AILadies?" **smazána** (obsah ikonek zachován – přesunut, viz níže).
- [ ] Fotografie Petry vložena na pravou stranu hero (portrétní, zaoblené rohy).
- [ ] Pod fotkou: jméno „Petra Květová Pšeničná" + popisek rolí.
- [ ] Logo plakety Women Changing the World vedle jména nebo v sekci O mně.
- [ ] Tlačítko 1: text změněn na „Konzultace zdarma (20 min)", stejný odkaz.
- [ ] Tlačítko 2: text změněn na „Jak mentoring probíhá →", stejný odkaz.
- [ ] Ikonky **1:1 / online / tvým tempem** přidány pod tlačítka na levé straně hero (přesunuto z dark karty – nestačí smazat, musí být vidět!).
- [ ] Pohyblivá lišta přidána pod hero, tmavé pozadí, zlatý/bílý text, plynulá animace.
- [ ] Stránka otestována na mobilu (lišta nesmí zastavit, foto nesmí přetékat, ikonky se zobrazí pod tlačítky).

---

## Co se NEMĚNÍ

- Barvy a font webu – beze změny.
- Ostatní sekce pod hero – beze změny.
- Formuláře a rezervační odkaz – beze změny.
- Obsah levé strany hero (nadpis, podtitul, eyebrow text) – beze změny, pouze texty tlačítek.
