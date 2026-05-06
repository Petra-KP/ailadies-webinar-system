# AILadies – Opravy a upřesnění instrukcí (kolo 2)

> Tento dokument **doplňuje a opravuje** původní instrukce v `AILadies_macaly_instrukce_2026.md`.
> Kde se tento dokument liší od původního, platí tento dokument.
>
> **Kontakt pro dotazy:** mentorka@ailadies.cz

---

## Přehled oprav

| # | Kde na webu | Co se opravuje |
|---|---|---|
| A | Sekce „Jak to funguje" | Upřesnění — co ponechat a co smazat (původní instrukce byly příliš radikální) |
| B | Sekce „Jak AI používám já" | Upřesnění layoutu 4 karet — změnit z 3+1 na mřížku 2×2 |
| C | Sekce „Hledáš jiný formát?" | Opravit text zpět na správné znění (Macaly použilo jiný text) |
| D | Auto-response e-mail — oslovení | Opravit malé písmeno a špatný pád jména (aktuálně „petra" místo „Petro") |
| E | Přepínač jazyka (EN) | Přesunout úplně vpravo za „Začít" + vizuálně utlumit |
| F | Anglická verze webu | Audit překladů — všechny sekce, formuláře, balíčky, patička, cookie lišta |

---

## A. Sekce „Jak to funguje" — upřesnění

> **Původní instrukce (sekce 3 v `AILadies_macaly_instrukce_2026.md`) říkala smazat vše včetně H2 a perexu. To je chybně. Platí toto upřesnění.**

### Co PONECHAT — beze změny

Tyto dva texty zůstávají na svém místě:

**H2 / nadpis sekce:**
```
Mentoring není přednáška. Je to společná práce na tvém konkrétním posunu.
```

**Perex pod H2:**
```
Každé sezení vychází z toho, co ty konkrétně potřebuješ.
```

### Co SMAZAT

Smazat pouze tyto prvky:

1. **Blok se čtyřmi kartami** (ikona + tučný text):
   - „Podíváme se na tvoji práci a najdeme, kde ti AI pomůže"
   - „Každé setkání navazuje na to předchozí"
   - „Rozvíjíme to, co už ti funguje"
   - „Odcházíš s řešením, které můžeš hned použít"

2. **Informační box** (box se světlým / zlatým pozadím a ikonkou ℹ) s celým textem:
   *„Mentoring funguje nejlépe tehdy, když ho přeneseš do praxe. Na našich setkáních ti ukážu směr, konkrétní postupy i nástroje, které můžeš hned použít. Skutečný posun pak přichází ve chvíli, kdy je začneš využívat ve své práci. Čím víc do toho dáš, tím víc si odneseš."*

### Co PŘIDAT — za perex

Za stávající perex („Každé sezení vychází z toho, co ty konkrétně potřebuješ.") přidat **callout box / citační blok**:

Vizuální styl: odlišit od okolního textu — zlatý levý rámeček nebo světle zlaté pozadí, kurzíva.

```
„Spousta lidí zná jen ChatGPT nebo Copilot a netuší, co dalšího existuje.
Ukážu ti, jaké nástroje se hodí přesně pro tvoji práci, a jak je správně použít."
```

### Výsledná podoba sekce po úpravě

```
[Label] Jak to funguje

[H2] Mentoring není přednáška. Je to společná práce na tvém konkrétním posunu.

[Perex] Každé sezení vychází z toho, co ty konkrétně potřebuješ.

[Callout box]
„Spousta lidí zná jen ChatGPT nebo Copilot a netuší, co dalšího existuje.
 Ukážu ti, jaké nástroje se hodí přesně pro tvoji práci, a jak je správně použít."
```

---

## B. Sekce „Jak AI používám já" — layout karet

### Aktuální stav (problém)
Sekce má 4 karty, ale jsou rozloženy jako **3 karty v horním řádku + 1 karta samotná v dolním řádku vlevo**. To vypadá nevyváženě.

### Co změnit — layout mřížky

Změnit rozložení karet ze 3 sloupců na **2 sloupce**, čímž vznikne symetrická mřížka **2 × 2**:

```
[ karta 1 ]  [ karta 2 ]
[ karta 3 ]  [ karta 4 ]
```

**V Macaly:** V nastavení bloku / sekce najít „Columns" nebo „Grid columns" a změnit hodnotu z `3` na `2`.

Na mobilním zobrazení ponechat 1 sloupec (karty pod sebou) — toto by mělo být výchozí chování builderu, neměnit.

**Pořadí karet ponechat stejné:**
1. Ze schůzky mám zápis dřív, než se zvedneme od stolu.
2. Můj styl, moje slova — jen mnohem rychleji.
3. Web od nápadu po spuštění — sama a s AI.
4. Faktury vystavuju v Google tabulkách a posílám z Gmailu.

---

## C. Sekce „Hledáš jiný formát?" — opravit text

### Aktuální stav (chybný text, který Macaly použilo)
```
Hledáš jiný formát?
Nabízím také setkání face-to-face nebo workshopy a přednášky pro týmy.
Napiš mi a společně najdeme to pravé řešení.
```

### Správné znění — opravit na toto

**Nadpis:**
```
Hledáš jiný formát?
```

**Dvě samostatné položky** (každá s ikonou šipky → nebo jiným vizuálním oddělovačem, titulek tučně + text pod ním):

→ **Setkání tváří v tvář**
```
Chceš se potkávat raději naživo? I to je možné. Domluvíme se individuálně.
```

→ **Mentoring pro tým**
```
AI by pomohla celému tvému týmu? Navrhnu spolupráci na míru.
```

**Tlačítko pod oběma položkami:**
```
Poptat nabídku →
```

Styl tlačítka: sekundární (outline), zlatý rámeček, stejná typografie jako ostatní sekundární CTA na stránce.

> **Poznámka:** Text „face-to-face", „workshopy a přednášky" ani „společně najdeme to pravé řešení" v zadání nejsou — použít výhradně znění uvedené výše.

---

---

## D. Auto-response e-mail — opravit oslovení

### Aktuální stav (chybný)
E-mail zobrazuje: **„Ahoj petra,"**

Dvě chyby:
1. Jméno začíná **malým písmenem** — má být velké: „Petra"
2. Jméno je v **1. pádu** (nominativ) — má být v **5. pádu** (vokativ): „Petro"

### Příčina
Macaly vkládá do e-mailu hodnotu pole „Jméno" tak, jak ji klientka napíše (malými písmeny, v základním tvaru). Systém automaticky český vokativ netvoří.

### Řešení

**Krok 1 — Opravit velké písmeno**

V nastavení e-mailové šablony v Macaly: u proměnné `{{first_name}}` nebo `{{jmeno}}` zapnout **„Capitalize"** (první písmeno velké). Toto musí fungovat — výsledek „petra" je nepřijatelný.

**Krok 2 — Správný 5. pád (vokativ)**

Macaly nebo vývojář musí zajistit automatický převod jména do vokativu pomocí vlastní funkce / skriptu. Pro česká ženská jména platí jasné pravidlo (viz tabulka níže) — řešením je lookup tabulka nebo funkce, která na základě jména z pole `{{first_name}}` vrátí správný vokativ.

Pokud Macaly toto nativně nepodporuje, obrátit se na jejich support s požadavkem: *„Potřebujeme v e-mailové šabloně zobrazit křestní jméno klientky v českém 5. pádě (vokativu) s velkým prvním písmenem."*

### Tabulka vokativů pro nejčastější česká ženská jména

Pro případ, kdy Macaly tým potřebuje orientaci:

| Jméno (1. pád) | Oslovení (5. pád) |
|---|---|
| Jana | Jano |
| Petra | Petro |
| Eva | Evo |
| Anna / Aneta | Anno / Aneto |
| Lenka | Lenko |
| Monika | Moniko |
| Tereza | Terezo |
| Lucie | Lucie |
| Marie | Marie |
| Martina | Martino |
| Kateřina | Kateřino |
| Veronika | Veroniko |
| Michaela | Michaelo |
| Markéta | Markéto |
| Zuzana | Zuzano |
| Alena | Aleno |
| Hana | Hano |
| Pavla | Pavlo |
| Barbora | Barbaro |
| Simona | Simono |

> Obecné pravidlo: ženská jména končící na **-a** → vokativ na **-o** (Jana → Jano). Jména končící na **-e** nebo **-ie** zůstávají stejná (Lucie → Lucie). Cizí jména obvykle také zůstávají (Jessica → Jessica).

### Výsledný správný e-mail

```
Ahoj [OSLOVENÍ v 5. pádu, velké první písmeno],

díky, že ses ozvala – tvoje poptávka mi právě dorazila.

Brzy se ti ozvu s návrhem spolupráce na míru.

Těším se!
Petra
AILadies · ailadies.cz · mentorka@ailadies.cz
```

**Příklad pro klientku Petru:**
```
Ahoj Petro,

díky, že ses ozvala – tvoje poptávka mi právě dorazila.
...
```

---

## E. Přepínač jazyka (EN) — pozice a vzhled

### Umístění v horní liště

**Požadavek:** Tlačítko / odkaz **„EN"** musí být **úplně vpravo** v navigaci — **až za** primárním tlačítkem **„Začít"**.

**Správné pořadí prvků v hlavičce (zleva doprava):**
```
[Logo AILadies]  [Pro koho] [Jak to funguje] [Co dostaneš] [Nabídka] [O mně] [FAQ …]  [Začít]  [EN]
```

Na mobilním menu stejná logika: „EN" jako **poslední položka** pod hlavním CTA, ne uprostřed mezi odkazy.

### Vizuální styl — méně výrazné než nyní

**Cíl:** Přepínač jazyka nesmí konkurovat tlačítku „Začít" ani hlavní navigaci.

Doporučené nastavení v Macaly:
- **Ne** používat výrazné zlaté / kulaté tlačítko jako u primárního CTA
- Použít **textový odkaz** nebo velmi jemný **ghost** styl: malé písmo (např. o 1–2 stupně menší než nav odkazy), barva **tlumená šedá** nebo **jemná zlatá** s nižší saturací
- Bez plného pozadí, případně jen **1px jemný border** v barvě okrajů stránky, nebo úplně bez rámečku
- Hover: lehké zesvětlení / podtržení — nic agresivního

**Kontrast:** Text „EN" musí zůstat čitelný (WCAG), ale vizuálně **sekundární** vůči „Začít".

---

## F. Anglická verze — kontrola překladů

Po každé úpravě českého obsahu je potřeba **vždy zkontrolovat anglickou verzi** (přepínač EN). Níže je checklist míst, kde často chybí překlady nebo zůstane čeština.

### Navigace a patička

- [ ] Všechny položky menu (Pro koho, Jak to funguje, Co dostaneš, Nabídka, O mně, FAQ, Začít)
- [ ] Patička — navigace, slogan, kontakt, právní řádek
- [ ] Odkazy „Zásady ochrany osobních údajů" / „Obchodní podmínky" — pokud jsou stránky jen v češtině, v EN verzi buď přeložit stránky, nebo jasně uvést „Czech only" / odkaz s vysvětlením

### Hero a sekce stránky

- [ ] Hero — eyebrow labely, H1, perex, všechna tlačítka (Konzultace zdarma, Jak mentoring probíhá, Chci osobní AI plán)
- [ ] Sekce problému / „Poznáváš se?"
- [ ] Sekce „Co jsem díky AI zvládla" / „Jak AI používám já" — všechny 4 karty (titulky + texty)
- [ ] Sekce „Jak to funguje" — H2, perex, callout o ChatGPT / Copilot
- [ ] Sekce „Co dostaneš" — všechny 4 karty
- [ ] Sekce „Nabídka" — nadpis, perex, úvodní konzultace, jednorázové setkání, **názvy a popisy balíčků** (Start / Rozjezd / Proměna + krátké podtitulky), ceny a slevy
- [ ] Sekce „Hledáš jiný formát?" — nadpis, obě položky, tlačítko „Poptat nabídku"
- [ ] Sekce „O osobní AI plán" / dotazník — nadpis, perex, tlačítko
- [ ] FAQ — všechny otázky i odpovědi
- [ ] Sekce „O mně" — bio, bullet pointy
- [ ] Sekce „Začít" / závěrečné CTA — kroky nebo texty vedoucí k formuláři

### Formuláře (kritické)

Projít **každý formulář** v anglické verzi:

- [ ] Hlavní kontaktní / poptávkový formulář (Začít) — názvy polí, placeholdery, povinné hvězdky, text souhlasu / GDPR checkboxu
- [ ] Formulář „Poptat nabídku" (Hledáš jiný formát?) — všechna pole včetně výběru typu poptávky (`Osobní setkání` / `Mentoring pro tým`)
- [ ] Tlačítka odeslání a **potvrzovací / chybové hlášky** po odeslání
- [ ] Texty tlačítek typu „Vybrat termín", „Chci mentoring" atd.

> **Pozn. k e-mailům:** Automatické e-maily z formuláře mohou zůstat v češtině, pokud tak klientka rozhodne — ale v případě anglicky vyplněné poptávky zvažovat anglickou šablonu nebo dvoujazyčný zápatí e-mailu.

### Cookie lišta

- [ ] Text banneru v EN
- [ ] Tlačítka (Přijmout / Odmítnout / Nastavení)
- [ ] Odkazy na privacy policy a terms

### Micelánní

- [ ] Tlačítko sdílení / „Zkopírovat odkaz" (pokud existuje)
- [ ] Jakýkoli pevný text v tlačítkách kalendáře (pokud je embednutý a lokalizovatelný)

### Postup testu

1. Otevřít web v **anonymním okně**, přepnout na **EN**
2. Projít stránku odshora dolů — vše musí být v angličtině (kromě schválně ponechaných vlastních názvů, např. „AILadies", „GitHub" — ty nepřekládat)
3. Odeslat **testovací odeslání** každého formuláře v EN režimu — ověřit hlášky
4. Po každé budoucí změně českého zdrojového textu **opakovat kontrolu EN**

---

## Checklist oprav (kolo 2)

- [ ] Sekce „Jak to funguje" — H2 a perex ponechány, pouze karty a info box smazány, callout přidán
- [ ] Sekce „Jak AI používám já" — layout změněn na 2×2, mobilní zobrazení ověřeno
- [ ] Sekce „Hledáš jiný formát?" — text opraven na správné znění (dvě položky + tlačítko)
- [ ] E-mailová šablona — jméno zobrazeno s velkým prvním písmenem a ve správném 5. pádu
- [ ] Přepínač „EN" — úplně vpravo za „Začít", vizuálně utlumený (sekce E)
- [ ] Anglická verze — audit překladů podle sekce F (navigace, sekce, formuláře, balíčky, cookie lišta)
- [ ] Po změnách znovu otestovat přepnutí CS ↔ EN

---

*Opravy kolo 2 · květen 2026 · mentorka@ailadies.cz*
