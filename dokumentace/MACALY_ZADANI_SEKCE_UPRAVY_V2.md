# Zadání pro Macaly: úpravy sekcí – AILadies (vlna 2)

**Stránka:** [ailadies.cz](https://www.ailadies.cz/)
**Tento dokument navazuje na:** `MACALY_ZADANI_HERO_REDESIGN.md`
**Rozsah:** 8 samostatných změn – každá popsána zvlášť

---

## Přehled změn

| # | Sekce | Co se mění |
|---|---|---|
| 1 | Hero | Ikonky 1:1 / online / tvým tempem přesunout hned za „✦ OSOBNÍ AI MENTORING“, zlatá barva, vyhodit popisky |
| 2 | Hero | Odstranit tmavý pruh pod tlačítkem „Jak mentoring probíhá" |
| 3 | Hero | Plaketa Women Changing the World – větší, přes okraj fotky |
| 4 | Hero | Jméno pod fotkou – opravit sirotek „Fandi mámám" |
| 5 | Hero + layout | Pohyblivá lišta výš + zmenšit mezeru nad hero |
| 6 | O mně | Vrátit portrét vlevo + text vpravo, nová fotka bez ořezu hlavy, vyhodit odrážky, nechat jen LinkedIn odkaz |
| 7 | Získej AI plán | Grafika PDF booklet – hravější, hover animace |
| 8 | Balíčky | Přidat úsporu v Kč pod každou cenu |

---

## Detailní popis každé změny

---

### Změna 1 – Ikonky 1:1 / online / tvým tempem: přesunout k řádku „OSOBNÍ AI MENTORING“

**Aktuální stav:**
Ikonky jsou umístěné dole vlevo pod tlačítky – v tmavém pruhu nebo pod hero jako tři sloupce.

**Nový stav:**
Ikonky přesunout **nahoru do horního eyebrow řádku**, tedy hned za text:
`✦ OSOBNÍ AI MENTORING`

Mají být ve stejné horní linii nad hlavním nadpisem „AI krok za krokem.“, ne u fotky a ne pod tlačítky.

**Barva:**
Zlatá – stejný odstín jako eyebrow text „✦ OSOBNÍ AI MENTORING" nad nadpisem.

**Co zachovat:**
```
1:1      online      tvým tempem
```

**Co vyhodit:**
Popisky pod ikonkami (`přizpůsobeno jen tobě`, `odkudkoliv`, `žádný spěch`) – **smazat**, nechat pouze tučné hodnoty.

**Výsledný vzhled horního řádku (přesný text):**
```
✦ OSOBNÍ AI MENTORING   ✦ 1:1   ✦ online   ✦ tvým tempem
```
Odděleno středníkem, zlatou tečkou nebo symbolem ✦ – stejný styl jako zbytek zlatých prvků webu.

---

### Změna 2 – Odstranit tmavý pruh pod tlačítkem „Jak mentoring probíhá"

**Aktuální stav:**
Pod tlačítkem „Jak mentoring probíhá →" je tmavý (černý) pruh/blok.

**Nový stav:**
Tmavý pruh **smazat úplně**. Pod tlačítky nenechávat žádný tmavý podklad.

---

### Změna 3 – Plaketa Women Changing the World: větší + přes okraj fotky

**Aktuální stav:**
Plaketa (zlatý medailon) je malá, umístěná jako malá ikona vedle jména.

**Nový stav:**
- Výrazně **zvětšit** – cca 90–110 px (nebo dle vlastního úsudku, ale musí být viditelná na první pohled).
- Umístit tak, aby **přesahovala přes okraj fotografie** (tzv. overlap) – ideálně vpravo dole nebo vpravo nahoře na fotce.
- Plaketa musí být klikatelná nebo alespoň vizuálně výrazná – zlatý medailon jako pečeť.

---

### Změna 4 – Jméno pod fotkou: opravit sirotek „Fandi mámám"

**Aktuální stav:**
Pod jménem Petry je text:
```
Mentorka AI · Moderátorka · Spoluzakladatelka
Fandi mámám
```
„Fandi mámám" je samo na druhém řádku – sirotek.

**Nový stav:**
Přeskládat text tak, aby „Fandi mámám" nebylo samo. Možné varianty (Macaly zvolí tu, která lépe sedí šířce sloupce):

**Varianta A – dva kratší řádky:**
```
Mentorka AI · Moderátorka
Spoluzakladatelka Fandi mámám
```

**Varianta B – oddělené odrážkami pod sebou:**
```
Mentorka AI
Moderátorka
Spoluzakladatelka Fandi mámám
```

**Varianta C – všechno na jednom řádku (pokud se vejde):**
```
Mentorka AI · Moderátorka · Spoluzakladatelka Fandi mámám
```

Zvolit variantu, která nevytváří sirotek a vizuálně sedí pod fotkou.

---

### Změna 5 – Pohyblivá lišta: přesunout výš + zmenšit mezeru nad hero

**A) Pohyblivá lišta – nová pozice:**

**Aktuální stav:** Lišta je úplně dole pod hero sekcí, mimo viditelnou část obrazovky při prvním načtení.

**Nový stav:** Přesunout lištu **těsně pod fotografii a jméno Petry** – tedy dovnitř hero sekce jako jeho spodní část, ne pod ní. Návštěvnice ji uvidí ihned po načtení stránky bez scrollování.

Pořadí prvků v hero (nové):
```
[NAV]
[Levý sloupec: horní řádek (OSOBNÍ AI MENTORING + 1:1/online/tvým tempem) + nadpis + text + tlačítka]
[Pravý sloupec: fotka + jméno + plaketa]
[LIŠTA – hned pod tím, přes celou šířku]
[další sekce...]
```

**B) Zmenšit mezeru nad hero:**

Pokud je nad hero nadpisem (nad textem „✦ OSOBNÍ AI MENTORING") příliš velká mezera (padding/margin shora), **zmenšit ji** – stránka by měla začínat obsah dříve, bez zbytečného prázdného prostoru pod navigací.
Doporučení: zmenšit padding-top hero sekce o cca 30–40 % oproti současnému stavu.

---

### Změna 6 – Sekce „O mně": nová fotka + úprava textu

**A) Nová fotka:**

Vrátit layout „O mně" do původního rozložení:
- **fotka vlevo**
- **text vpravo**

Aktuální problém je, že použitá fotka je oříznutá tak, že není vidět hlava.
Proto použít portrétní záběr (na výšku) a jemný ořez tak, aby byl vidět celý obličej.

- Vložit místo stávající fotky v sekci O mně.
- Rozložení ponechat vedle sebe: fotka vlevo, text vpravo (jako dřív).
- Fotka má být na výšku (doporučený poměr 4:5 nebo 3:4), ne široký banner.
- Ořez nastavit tak, aby hlava nebyla useknutá (`object-position: center top` nebo ekvivalent v Macaly).
- Zaoblené rohy zachovat (stejné jako ostatní fotky na webu).
- Použít aktuální soubor: `01_PROJEKTY/AILadies/assets/petra_o_mne_fotka_portrait_667x1000.png`
- Referenční formát dodané fotky je **667 × 1000 px** (portrét). Tento poměr zachovat i v zobrazení na webu.

**B) Vyhodit odrážky:**

Aktuálně jsou v sekci O mně odrážky s hvězdičkami ✦:
```
✦ Fandi mámám – spoluzakladatelka
✦ Moderování & facilitace
✦ AI vzdělávání – Aibility
✦ Podcast Dobro skladem
✦ Mediální tréninky
```

**Celý tento blok odrážek smazat.**

**C) Nechat pouze LinkedIn odkaz:**

Z celého spodního bloku zachovat pouze:
```
→ LinkedIn profil
```
Odkaz: `https://www.linkedin.com/in/petra-kv%C4%9Btov%C3%A1-p%C5%A1eni%C4%8Dn%C3%A1/`

Styl: zachovat jako je nyní – šipka + text, zlatá nebo tmavá barva dle webu.

---

### Změna 7 – Sekce „Získej svůj osobní AI plán": hravější grafika booklet

**Aktuální stav:**
Pravá část sekce je pravděpodobně prázdná nebo má jen jednoduchý prvek.

**Nový stav:**
Přidat grafiku ve stylu **nakloněného PDF sešitu/kartičky**, která se na hover narovná – vizuálně napovídá, že jde o dokument ke stažení.

**Popis grafiky – co zobrazit (text musí odpovídat Osobnímu AI plánu, ne promptům):**

```
┌──────────────────────┐
│ OSOBNÍ AI PLÁN · PDF │  ← malé zlaté písmo nahoře
│                      │
│  Tvůj plán na míru   │  ← větší serif nadpis
│  kde začít s AI      │
│  a co řešit jako     │
│  první krok          │
│                      │
│  ─────────────────   │  ← dekorativní linky (napodobují text)
│  ───────────         │
│  ─────────────────   │
│  ───────────         │
│                      │
│  stručně a prakticky │  ← malý text dole
│  bez technického     │
│  balastu             │
└──────────────────────┘
```

**Parametry kartičky:**
- Barva: bílá nebo velmi světlá (cream), jemný stín.
- Okraje: zaoblené (rounded corners).
- Rotace v klidovém stavu: cca **–3 stupně** (mírně nakloněná doleva).
- Rotace na hover: **0 stupňů** – plynulé narovnání (CSS transition 0.3s ease).
- Stín: výraznější při hoveru (shadow-lg efekt).

**Instrukce pro Macaly:**
Pokud není dostupná přímá CSS/custom animace, lze použít:
- Macaly „Card" komponent + vlastní CSS třída pro rotaci.
- Nebo jako statický obrázek (Petra dodá PNG mockup) bez animace – jako záložní řešení.

**Text sekce „Získej svůj osobní AI plán" zachovat beze změny** – mění se pouze vizuální prvek vpravo.

**Důležité:** Do kartičky už nedávat jméno „Petra Květová Pšeničná".

---

### Změna 8 – Balíčky: přidat úsporu v Kč pod každou cenu

Pod každou cenu balíčku přidat text s úsporou. Styl: menší písmo, zlatá nebo zelená barva – vizuálně odlišit od hlavní ceny.

| Balíček | Cena | Text k přidání |
|---|---|---|
| Start (3 setkání) | 8 550 Kč | `ušetříš 450 Kč` |
| Rozjezd (5 setkání) | 13 800 Kč | `ušetříš 1 200 Kč` |
| Proměna (10 setkání) | 26 100 Kč | `ušetříš 3 900 Kč` |

**Umístění:** přímo pod číslem ceny, před nebo za dalším popisným textem balíčku.

**Poznámka:** Pokud jsou úspory na webu již zobrazeny (byly součástí dřívějšího zadání), tuto změnu přeskočit – pouze zkontrolovat, že jsou správně zobrazeny u všech tří balíčků.

---

## Vizuální schéma hero po všech úpravách

```
[NAV]
├─────────────────────────────────────────────────────┤
│  (menší mezera nahoře)                              │
│  ✦ OSOBNÍ AI MENTORING ✦ 1:1 ✦ online ✦ tvým tempem│
│                                                     │
│  AI krok za krokem.       ┌───────────────────┐     │
│  Tvým tempem.             │                   │     │
│  S viditelnými výsledky.  │   FOTKA PETRY     │  🏅 │ ← plaketa přes okraj
│                           │                   │     │
│  Osobní mentoring pro...  │  Petra Květová    │     │
│                           │  Pšeničná         │     │
│  [Konzultace zdarma]      │  Mentorka AI ·    │     │
│  [Jak mentoring probíhá]  │  Moderátorka ·    │     │
│                           │  Spoluzakladatelka│     │
│                           │  Fandi mámám      │     │
│                           └───────────────────┘     │
├─────────────────────────────────────────────────────┤
│  ✦ AI nadšenkyně ✦ Mentorka AI ✦ Moderátorka ✦...  │ ← LIŠTA (hned viditelná)
├─────────────────────────────────────────────────────┤
│  (další sekce...)                                   │
```

---

## Checklist pro Macaly

**Hero:**
- [ ] Ikonky 1:1 / online / tvým tempem přesunuty do horního řádku za text „✦ OSOBNÍ AI MENTORING“, zlatá barva, popisky odstraněny.
- [ ] Tmavý pruh pod tlačítky odstraněn.
- [ ] Plaketa zvětšena (90–110 px), přes okraj fotky.
- [ ] Sirotek „Fandi mámám" opraven – vhodné přeskládání textu.
- [ ] Pohyblivá lišta přesunuta těsně pod hero (viditelná bez scrollování).
- [ ] Mezera nad hero nadpisem zmenšena (méně prázdného prostoru pod nav).

**O mně:**
- [ ] Stará fotka nahrazena novou portrétní fotkou (na výšku), hlava nesmí být oříznutá.
- [ ] Rozložení sekce O mně vráceno na „fotka vlevo, text vpravo".
- [ ] Odrážky ✦ (Fandi mámám, Moderování, AI vzdělávání, Podcast, Mediální tréninky) smazány.
- [ ] Zachován pouze LinkedIn odkaz.

**Lead magnet:**
- [ ] Grafika PDF sešitu přidána vpravo v sekci – nakloněná –3°, na hover se narovná.

**Balíčky:**
- [ ] Pod Start: `ušetříš 450 Kč`
- [ ] Pod Rozjezd: `ušetříš 1 200 Kč`
- [ ] Pod Proměna: `ušetříš 3 900 Kč`

---

## Co se NEMĚNÍ

- Texty nadpisů a odstavců – beze změny.
- Barvy, fonty a celkový styl webu – beze změny.
- Formuláře, rezervační odkazy, struktura ostatních sekcí – beze změny.
