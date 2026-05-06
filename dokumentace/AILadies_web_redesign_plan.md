# AILadies – Plán redesignu webu

> Kompletní fázovaný plán úprav pro www.ailadies.cz.
> Výstup: texty, paleta, struktura sekcí, FAQ a checklist pro Macaly.
> Doplněno o novou HTML referenční stránku v `aplikace/index_v2.html`.

---

## 1. Shrnutí analýzy

### Co funguje (nech být)
- **Tón textů** – tykání, empatie, žádný tech hype. Sedí na cílovku.
- **„Nejsem programátorka. Jen zkouším…"** – autentické, klíčová věta celé stránky.
- **Sekce s námitkami** („Zkusila jsem to, ale nefunguje to…") – výborný copywriting.
- **Konkrétní use-casy** (smlouvy, faktury, granty, web) – nejsilnější část webu.
- **Úvodní konzultace zdarma** – perfektní konverzní háček.

### Co nefunguje (5 hlavních slabin)
1. **Moc textu nad záhybem** – hero je dlouhý, návštěvnice nestihne pochopit benefit.
2. **Chybí sociální důkaz** – žádné reference, loga, čísla. U cen 8 550–26 100 Kč je to kritické.
3. **Rozmlžená CTA hierarchie** – 6+ tlačítek, žádné není vizuálně „to hlavní".
4. **U balíčků není vidět úspora** – chybí „ušetříš X Kč" proti jednorázovým 3 000 Kč/h.
5. **Chybí FAQ, garance, „pro koho to NENÍ"** – návštěvnice odchází s pochybnostmi.

### Persona – Jana (38, HR/marketing/majitelka malého byznysu)
- **Co ji osloví:** tón, konzultace zdarma, use-casy v jejím světě (smlouvy, faktury).
- **Kde zaváhá:**
  - „3 000 Kč/hodina je hodně, vrátí se mi to?" → chybí ROI.
  - „Bude mě soudit, že neumím?" → řešeno textem, chce to i vizuál (uvolněná fotka, ne korporátní).
  - „Co když se nedomluvíme?" → pomohla by garance / peníze zpět.
- **Dožene ji ke konverzi:** konzultace zdarma + 1 reference od „ženy jako ona".

---

## 2. Barevná paleta

### Doporučená: Warm Terracotta

| Role | HEX | Použití |
|---|---|---|
| Background base | `#FBF8F4` | Pozadí stránky, off-white (ne sterilně bílá) |
| Background alt | `#F2E9DE` | Každá druhá sekce, karty |
| Primary text | `#1F1B16` | Nadpisy, tělo textu (teplá tmavá, ne černá) |
| Muted text | `#6B5E52` | Popisky, metadata |
| Primary accent | `#B8654F` | CTA tlačítka, podtržení, aktivní stavy |
| Primary hover | `#9F4F3B` | Hover na CTA |
| Secondary accent | `#2E4A3C` | Sekundární CTA, ikony, citáty |
| Highlight | `#E8D5C4` | Badge, pill, „nejčastější volba" |
| Border | `#E5D8C8` | Okraje karet, oddělovače |

### Alternativa: Dusty Rose (pokud chceš víc feminní)
- Primary accent: `#C68A8A` místo terracotta
- Secondary: `#6B4A5C` (soft plum)
- Zbytek palety stejný.

### Typografie
- **Nadpisy:** `Fraunces` (serif, variable, zdarma na Google Fonts) – moderní, ženský, seriózní.
- **Tělo:** `Inter` nebo `DM Sans` (sans-serif, čitelné).
- **Akcenty / eyebrow:** Stejný sans, ale `letter-spacing: 0.15em; text-transform: uppercase; font-size: 0.75rem`.

**V Macaly:** obě jsou v katalogu Google Fonts, stačí vybrat a přiřadit k rolím Headline / Body.

---

## 3. FÁZE 1 – Rychlé výhry (must-have)

### 3.1 Hero – nový text

**Eyebrow:**
```
AI MENTORING PRO ŽENY · 1:1 ONLINE · ČESKY
```

**Nadpis (hlavní):**
```
AI, která ti konečně
začne šetřit čas.
```

**Podtitul:**
```
Osobní 1:1 mentoring pro ženy, které chtějí AI používat v práci —
bez kurzů, bez chaosu, vlastním tempem.
```

**CTA primární:** `Konzultace zdarma (20 min)`
**CTA sekundární:** `Jak mentoring probíhá →`

**Trust řádek pod CTA (malý text s ikonami):**
```
★★★★★  Už 30+ žen  ·  Spoluzakladatelka Fandi mámám  ·  Moderátorka ČT/ČRo
```
*(čísla a média dopiš podle reality)*

---

### 3.2 Reference – šablona

Přidej sekci **hned pod hero** (3 karty vedle sebe). Šablona pro každou kartu:

```
„{Konkrétní citát – 1–2 věty o tom, co jí mentoring dal.}"

— {Jméno}, {obor/role}
   {1 věta o výsledku: např. „Ušetřila 4 hodiny týdně na fakturaci."}
```

**E-mail, který pošleš stávajícím klientkám (pro získání reference):**

> Ahoj {jméno},
>
> dávám dohromady reference na nový web AILadies a byla bych moc ráda za pár řádků od tebe. Nemusí to být nic formálního — stačí odpovědět na tohle:
>
> 1. Co jsi řešila, než jsme začaly pracovat spolu?
> 2. Co ti mentoring konkrétně dal (v čase, klidu, nebo penězích)?
> 3. Komu bys ho doporučila?
>
> Pošlu ti finální verzi ke schválení, než to dám na web. A kdyby to šlo, přidala bych i tvoji fotku a jméno — dodá to důvěru jiným ženám.
>
> Díky moc! P.

---

### 3.3 FAQ sekce – 8 hotových otázek

```
❓ Co když s AI neumím vůbec nic?
To je nejlepší výchozí pozice. Nemusíš nic umět. Začneme u toho, co
reálně děláš v práci, a ukážu ti, kde ti AI pomůže od prvního dne.

❓ Jaký nástroj budeme používat?
Hlavně ChatGPT (většinou stačí placená verze za ~500 Kč/měsíc),
podle potřeby pak Gemini, Notebook LM, Claude nebo automatizace přes
Google. Vždy volíme to, co ti dává smysl — žádné předplatné navíc,
pokud ho nepotřebuješ.

❓ Musím mít placené ChatGPT?
Pro první hodinu ne. Pokud se rozhodneme, že AI chceš používat
pravidelně, placená verze se většinou vyplatí. Poradím ti, kdy má
smysl platit a kdy stačí free.

❓ Je to pro mě, i když nemám firmu?
Ano. Mentoring funguje pro zaměstnankyně, freelancerky, neziskovky
i maminky na mateřské, které plánují návrat. Pracujeme s tím, co
řešíš ty — ne s obecnými příklady.

❓ Co když se nesejdeme — mohu peníze dostat zpět?
Úvodní konzultace (20 min) je zdarma, tak si nejdřív vyzkoušíme,
jestli si sedneme. Pokud by tě i tak první placená hodina
nenadchla, peníze vrátím bez diskuse.

❓ Jak dlouho trvá jeden balíček?
Start (3 setkání) obvykle 4–6 týdnů, Rozjezd (5 setkání) 2–3 měsíce,
Proměna (10 setkání) 4–6 měsíců. Tempo si řídíš ty.

❓ Kdy a kde sezení probíhají?
Online (Google Meet nebo Zoom), v čase, který si vybereš v mém
kalendáři. Většinou dopoledne nebo odpoledne všedních dnů.

❓ Co když nestíhám pracovat mezi sezeními?
V pohodě. Tempo mentoringu přizpůsobíme tvému životu, ne naopak.
U balíčků máš 5 dní po sezení e-mailovou podporu, když se zasekneš.
```

---

### 3.4 Balíčky – přepsané

| Balíček | Cena | Úspora | Doba trvání | Pro koho |
|---|---|---|---|---|
| **Start** (3 setkání) | 8 550 Kč | *ušetříš 450 Kč* | 4–6 týdnů | Pochopíš, jak AI zapojit do dne |
| **Rozjezd** (5 setkání) ⭐ | 13 800 Kč | *ušetříš 1 200 Kč* | 2–3 měsíce | Začneš AI reálně používat v práci |
| **Proměna** (10 setkání) | 26 100 Kč | *ušetříš 3 900 Kč* | 4–6 měsíců | Nastavíš si vlastní systém |

⭐ **Nejčastější volba** – vizuálně vyzdvihnout (jiná barva pozadí karty, badge).

---

### 3.5 Drobnosti
- Odstranit `👉` emoji z tlačítek – nahradit `→` nebo čistým textem.
- Všechna primární CTA sjednotit: plné terracotta pozadí, bílý text, radius `50px` (pill), hover = ztmavení.
- Sekundární CTA: outline (1px border) stejné barvy, transparentní pozadí.

---

## 4. FÁZE 2 – Vizuální přestavba

### 4.1 Mapa barev po sekcích

| Sekce | Pozadí | Text | Akcent |
|---|---|---|---|
| Nav | `#FBF8F4` s blur | `#1F1B16` | `#B8654F` |
| Hero | `#FBF8F4` | `#1F1B16` | `#B8654F` |
| Reference | `#F2E9DE` | `#1F1B16` | `#2E4A3C` |
| Use-cases (bento) | `#FBF8F4` | `#1F1B16` | `#B8654F` |
| Jak to funguje | `#F2E9DE` | `#1F1B16` | `#2E4A3C` |
| Balíčky | `#FBF8F4` | `#1F1B16` | `#B8654F` |
| FAQ | `#F2E9DE` | `#1F1B16` | `#2E4A3C` |
| O mně | `#1F1B16` (tmavá!) | `#FBF8F4` | `#E8D5C4` |
| Finální CTA | `#B8654F` | `#FBF8F4` | bílá |
| Footer | `#1F1B16` | `#FBF8F4` | `#B8654F` |

Střídání light / alt / light vytváří rytmus a „vede oko".

### 4.2 Hero layout
- **Desktop:** 60/40 split – vlevo text, vpravo tvoje fotka (portrét, ne stock, teplé světlo). Na fotce lehký terracotta overlay 10 % pro jednotu s paletou.
- **Mobil:** fotka nahoře (1:1 čtverec), text pod ní.

### 4.3 Bento grid – „Co jsem díky AI zvládla"
6 karet v mřížce 3×2 (desktop) / 2×3 (tablet) / 1 sloupec (mobil).

Každá karta:
- Ikona (Lucide, Phosphor nebo vlastní SVG) v terracotta.
- Nadpis (1 věta, 6–8 slov).
- Popis (2–3 věty).

Karty (texty už existují na webu, jen zkrátit):
1. **Smlouvy píše AI** – Popíšu situaci, dostanu návrh, uložím na disk.
2. **Faktury v Google tabulkách** – Bez předplatného, bez systému navíc.
3. **AI asistent na granty** – Žádosti rychleji a bez stresu.
4. **Můj styl, moje slova, rychleji** – Články, scénáře, LinkedIn.
5. **Web od nápadu po launch** – Tenhle, co právě čteš.
6. **Zápis ze schůzky za 3 minuty** – Přepis, úkoly, prezentace.

### 4.4 „Pro koho to JE / NENÍ" blok

Dvousloupcová sekce s checkmarky a křížky.

**Mentoring je pro tebe, když:**
- ✓ Pracuješ s texty, daty, klientkami nebo dokumenty.
- ✓ Chceš přestat ztrácet čas opakovanou prací.
- ✓ AI jsi zkusila, ale pořád ji nepoužíváš pravidelně.
- ✓ Chceš někoho, kdo tě tím provede česky a lidsky.

**Mentoring není pro tebe, když:**
- ✗ Programuješ a AI už denně používáš na víc věcech.
- ✗ Hledáš technický kurz o LLM a prompt engineeringu.
- ✗ Očekáváš, že za tebe vše udělám (mentoring = společná práce).

### 4.5 Video v „O mně" – scénář 45 s

```
(0:00–0:10) Kdo jsi: „Ahoj, jsem Petra. Moderátorka, mamka,
spoluzakladatelka neziskovky Fandi mámám."

(0:10–0:25) Příběh: „Dlouho jsem si myslela, že AI není pro mě.
Pak jsem ji zkusila — a změnilo mi to způsob práce. Dneska díky
ní zvládnu za hodinu to, co mi dřív zabralo celý den."

(0:25–0:40) Nabídka: „A tohle teď ukazuju jiným ženám. Bez tech
žargonu, přesně na to, co řešíš ty."

(0:40–0:45) CTA: „Prvních 20 minut je zdarma. Tak si pojďme
povídat."
```

Natočit telefonem na stativ, dobré denní světlo, klidné pozadí. Titulky přidat v CapCut nebo přes AI (Descript).

---

## 5. FÁZE 3 – Konverzní dotažení

### 5.1 Lead magnet: „10 promptů, které používám denně" (PDF)

**Osnova PDF (8 stran, A4, stejná paleta jako web):**

1. Úvod – proč 10 promptů (1 strana).
2. Prompty pro texty: článek, LinkedIn, e-mail klientce (2 strany).
3. Prompty pro smlouvy a dokumenty (1 strana).
4. Prompty pro shrnutí a přípravu na schůzky (1 strana).
5. Prompty pro učení a research (1 strana).
6. Bonus: 3 prompty pro osobní věci (rodina, cestování, kariéra) (1 strana).
7. Závěr + CTA na konzultaci zdarma (1 strana).

**Text na landing blok:**
```
Nechceš rovnou mentoring? Stáhni si zdarma

→ 10 promptů, které používám denně

  Hotové texty, které jen zkopíruješ do ChatGPT a hned uvidíš
  rozdíl. Žádný spam — jen 3 e-maily s kontextem, jak prompty
  používat.

  [Tvůj e-mail]   [Chci prompty zdarma →]
```

**E-mailová sekvence (3 e-maily po zadání e-mailu):**

**E-mail 1 (ihned):** „Tvé prompty jsou tady"
- Odkaz na PDF + krátký úvod + jemný CTA na konzultaci.

**E-mail 2 (+2 dny):** „Který prompt ti nejvíc sednul?"
- Krátký osobní dotaz + story, jak konkrétní prompt používá ona + CTA „pokud chceš víc takových věcí šitých na míru, pojď na konzultaci zdarma".

**E-mail 3 (+5 dnů):** „Pokud ti to dává smysl…"
- Shrnutí: pokud tě prompty baví, tady je konzultace zdarma (20 min). Měkký close, žádný tlak.

### 5.2 Sticky CTA bar (mobil)

Zobrazit po scrollu > 400 px:
```
Konzultace zdarma (20 min)  →
```
- Pozadí: `#B8654F`, text bílý, celá šířka, výška 56 px, fixovaný dole.
- Po kliknutí otevřít Google Calendar rezervaci.

### 5.3 Trust bar pod hero

Řádek s nadpisem „Jak o mně píšou" + 4–6 log (ČT, ČRo, Forbes, Fandi mámám, Aibility, podcast Dobro skladem).
- Loga v odstínu šedé (filter: grayscale), na hover plná barva.
- Na mobilu jako horizontální carousel.

### 5.4 Footer (rework)

```
AILADIES
Osobní AI mentoring pro ženy

Sekce:            Kontakt:             Projekty:
Jak to funguje    petra@ailadies.cz    Aibility
Balíčky           IČO: 00000000        Fandi mámám
FAQ               Praha, ČR            Dobro skladem (podcast)
Reference                              LinkedIn
O mně

---
© 2026 Petra Květová Pšeničná · Obchodní podmínky · Zpracování údajů
```

### 5.5 Garance (volitelně, ale silně doporučuju)

Umístit na stránku balíčků:
```
★ Garance spokojenosti

Pokud tě po první placené hodině mentoring nenadchne,
vrátím ti peníze bez otázek. Tvé riziko = nula.
```

---

## 6. Checklist pro Macaly

Pořadí úprav, aby ses v editoru neztratila:

### Fáze 1 (1 večer)
- [ ] Zálohuj aktuální verzi stránky (duplikace v Macaly).
- [ ] V „Theme / Colors" nastav paletu (HEX z kapitoly 2).
- [ ] V „Theme / Typography" napáruj Fraunces (H1-H6) + Inter/DM Sans (body).
- [ ] Přepiš **hero** text (eyebrow + H1 + podtitul + 2 CTA + trust řádek).
- [ ] Sjednoť styl CTA tlačítek (primární full, sekundární outline, pill radius).
- [ ] Odstraň všechny `👉` emoji, nahraď `→`.
- [ ] V balíčcích přidej úsporu a badge „Nejčastější volba".
- [ ] Přidej sekci **Reference** (zatím 3× placeholder, dokud nedorazí e-maily od klientek).
- [ ] Přidej sekci **FAQ** (8 otázek z kapitoly 3.3).

### Fáze 2 (1–2 večery)
- [ ] Vyměň hero obrázek za portrét (foť v denním světle, teplé tóny).
- [ ] Přestav „Co jsem díky AI zvládla" na **bento grid 3×2**.
- [ ] Přidej blok **„Pro koho to JE / NENÍ"** pod FAQ.
- [ ] Sekci **O mně** předělej na tmavé pozadí (`#1F1B16`).
- [ ] Natoč video 45 s, vlož do „O mně" jako hlavní vizuál.

### Fáze 3 (průběžně)
- [ ] Vytvoř PDF „10 promptů" (v Canva nebo AI).
- [ ] Nasaď e-mail form (Mailchimp / Smartemailing / ActiveCampaign).
- [ ] Naprogramuj 3-e-mailovou sekvenci.
- [ ] Přidej sticky CTA bar (mobil only).
- [ ] Doplň trust bar s logy pod hero.
- [ ] Přepis footer.
- [ ] (Volitelně) Přidej garanci k balíčkům.

---

## 7. HTML referenční stránka

V `aplikace/index_v2.html` najdeš **hotovou implementaci celého redesignu** v jednom HTML souboru. Slouží jako:
- **Vizuální reference** – jak má web vypadat po úpravách.
- **Copy-paste zdroj textů** – všechny texty z tohoto plánu jsou tam „zalité" do hotové stránky.
- **Ukázka pro tebe i pro klientky** – můžeš ji otevřít lokálně v prohlížeči a procházet.

Otevři si ji poklepáním v průzkumníkovi nebo přes `Start-Process "01_PROJEKTY\AILadies\aplikace\index_v2.html"` v PowerShellu.

---

## 8. Co se v plánu zámerně NEŘEŠÍ

- **Implementace v Macaly** – nemám do Macaly přístup; provedeš dle checklistu sama.
- **Reálné fotky** – v HTML jsou placeholdery (CSS kruh s iniciálami). Nahraď je svými foto.
- **Skutečná loga médií** – v HTML jsou textové placeholdery.
- **Technická SEO analýza** – řeší se až po obsahové stabilizaci (fáze 3+).
